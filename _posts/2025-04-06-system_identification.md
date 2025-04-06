---
title: 'Modelling and system identification: how to apply it in identifying your potential lover'
date: 2025-04-06
permalink: /posts/2020/11/system_identification/
excerpt_separator: <!--more-->
usemath: true
tags:
  - Scientific story
  - Mathematic
  - Control
---
Trong điều khiển có một chủ đề rất quan trọng nhưng ít được quan tâm đúng mức đó là “mô hình hóa và nhận dạng hệ thống”. Đại loại là để điều khiển bất kể đối tượng nào thì bước đầu tiên là phải hiểu được đối tượng đó hoạt động như thế nào. Kiểu như thanh niên muốn chinh phục một cô gái, mà không hiểu đối tượng mình đang tán, tâm tư tình cảm cô gái ấy như thế nào mà vội vả ra hành động là hỏng ngay. 

Sau bao nhiêu năm làm về điều khiển, hôm vừa rồi ngồi chém gió với mấy cậu đồng nghiệp trẻ trong công ty để truyền bí kíp về chủ đề này.

<!--more-->

Bí kíp thì từ nhiều nơi nhưng muốn học bài bản phải đọc cuốn “system identification” của Lenart Lijung. Cụ Lijung không chỉ nói về lý thuyết mà còn cha đẻ của system identification toolbox trong matlab để giúp người dùng ứng dụng nó. Vấn đề là sách này rất nặng về toán, và nếu ai chưa hiểu nhiều về chủ đề này vào đọc thì rất dễ nản. Bản thân mình bắt đầu đụng cuốn này thời bắt đầu làm master về process control (từ năm 2012) nhưng hồi đó sau khi đọc được mấy hôm thì lại quăng đi vì lúc đó mới vào nghề tự học lơ ngơ chả hiểu được nhiều nên chán, sau này dần hiểu ý nghĩa nên đọc kỷ hơn và thấy quan trọng. Hôm vừa rồi có buổi thảo luận về mô hình hóa và nhận dạng các tham số cho UAVs, thế là giới thiệu cuốn này cho mấy chú đồng nghiệp, chém thêm một vài ý trong đó liên hệ với chuyện yêu đương trai gái cho mấy chú dễ hình dung, chứ mới đâm đầu vào mà đụng toán nhiều là dễ bỏ ngay.

Cơ bản sách có 3 phần chính trong đó Phần 1 và Phần 2 là nền tảng còn Phần 3 là ứng dụng. 

Phần 1 sách nói về các mô hình toán dùng để mô tả hệ thống/đối tượng chúng ta muốn điều khiển. Lấy ví dụ chúng ta có hệ thống là chiếc xe hơi và chúng ta muốn điều khiển nó chạy ở một vấn tốc mong muốn (60km/h chẳng hạn). Để làm được điều này bước đầu tiên là phải hiểu được mối liên hệ giữa chân ga (đầu vào) và đầu ra (vận tốc) của hệ thống (chiếc xe hơi) như thế nà. Bước này còn gọi là mô hình hóa và nhận dạng hệ thống. Để làm điều này có ba cách: 

1) Cách 1 dùng các định luật Newton hay Lagrange để viết hệ các phương trình vi phân mô tả nó. Biết được chính xác các tham số như khối lượng, hệ số ma sát không khí, vv … thì coi như chúng ta có thể có được mô hình toán hoàn chỉnh để hiểu được chiếc xe hoạt động như thế nào. Mô hình toán này còn gọi là mô hình trắng (white box model) vì chúng ta thấy và biết được hoàn toàn bên trong mô hình như thế nào.

2) Cách 2 tương tự như cách 1, đó là chúng ta có hệ phương trình vi phân mô tả hệ thống rồi nhưng giả sử hệ số ma sát không khí không biết được chúng ta cần phải dùng dữ liệu để tìm nó. Mô hình này còn được gọi là grey-box model

3) Cách thứ 3 là trong trường hợp không có hệ phương trình mô tả mối quan hệ giữa đầu vào và đầu ra, chúng ta giả sử mối liên hệ này được xấp xỉ bởi một mô hình nào đó có cấu trúc có thể là transfer function, state-space, neuron network … rồi bước tiếp theo là dùng data từ ngõ vào (vị trí của chân ga) và đầu ra (vận tốc) để nhận dạng các tham số bên trong mô hình này. Ví dụ tham số của state-space model cho hệ tuyến tính là các ma trận A,B,C,D, còn neuron network là các trọng số, vv. Mô hình thứ 3 này người ta gọi là black-box vì cơ bản chúng ta không biết bên trong nó như thế nào.


Phần 2 của sách dùng để nói về các phương pháp làm sao để để nhận dạng (hay nói cách khác ước lượng) các tham số của mô hình từ dữ liệu đầu vào và đầu ra của hệ thống.  

Phần 3 có lẽ là quan trọng nhất và mong chờ nhất cho những ai muốn ứng dụng ngay mô hình hóa và nhận dạng hệ thống vào công việc của mình, đó là giả sử hệ thống là chiếc xe hơi với ngõ vào vị trí chân ga, và ngõ ra là vận tốc làm sao có thể xây dựng được mô hình chiếc xe chỉ dựa vào data từ chân ga và vận tốc đo được ? 

Với bài toán này câu trả lời là dùng phương pháp black-box model, tiến hành theo các bước sau với công cụ system identification (SysID) của matlab.

Bước 1: chọn một mô hình nào đó phù hợp cho hệ thống, ví dụ như mô hình có dạng một transfer function (hàm truyền) bậc 2 chẳng hạn với đầu vào là vị trí chân ga, đầu ra là vận tốc.   

Bước 2: là nhận dạng tham số của mô hình này, đó là các hệ số ở tử số và mẫu số của hàm truyền đã chọn. Để đạt được điều này với SysID toolbox của matlab thì trước hết phải chuẩn bị data của ngõ vào và ngõ ra. Vậy data này lấy từ đâu ? Data này có thể lấy được bằng cách lấy chiếc xe ra, nhấn chân ga lên xuống và đo và lưu lại vị trí của chân ga và vận tốc. Nhưng nên nhấn chân ga như thế nào để data chứa nhiều thông tin nhất về hệ thống, bởi vì nếu data “nghèo thông tin” thì dù cấu trúc mô hình chọn chuẩn như thế nào thì sau khi ước lượng cũng không thể miêu tả được các đặc tính của hệ thống ? Vậy làm sao để data này có nhiều thông tin nhất có thể, điều đó phụ thuộc vào cách chúng ta nhấn chân ga, tức là thiết kế tính hiệu cho ngõ vào hệ thống - và phần này gọi là experimental design trong sách của Lijung. 

Đơn giản nhất là chúng ta nhấp ga rồi giữ ở mức nào đó (ví dụ 30% của ga) sau đó đợi và đo vân tốc đáp ứng. Input kiểu này đơn giản và rất hữu dụng cho các đối tượng trong process control (như điều khiển nhiệt độ, hóa dầu) và thậm chí cho vị dụ điều khiển tốc độ nêu trên nhưng rõ ràng dữ liệu thu được không phản ánh hết đặc tính của chiếc xe. Vì sao ? Vì với step input chúng ta chỉ hiểu được đáp ứng của hệ thống ở trạng thái đã ổn định (steady-state) chứ chúng ta không biết được đáp ứng vận tốc sẽ như thế nào nếu chúng ta nhấp ga lên xuống liên tục (tức tần số ngõ vào thay đổi). Cũng như tương tự trong nhận dạng cô gái, bạn mời cô ấy đi cafe một lần (ie. step input) rồi quan sát cô ấy cư xử thì chỉ chừng đấy bạn không thể nào hiểu biết đầy đủ cô gái đó.

Để khắc phục điều này, chúng ta phải thiết kế tính hiệu ngõ vào sao cho kích thích hệ thống hơn. Một trong những tính hiệu đó có thể là dạng sinusoid, tức là đạp chân ga từ từ lên rồi từ từ xuống theo một chu kỳ nào đó rồi xem vận tốc xe đáp ứng như thế nào. Như vậy với mỗi tần số đạp ga nhất định chúng ta biết được vận tốc đáp ứng thế nào. Để hiểu được vận tốc đáp ứng ở các tần số khác nhau nữa ta lại trộn thêm vào nhiều sóng sines ở chân ga. Tương tự, để hiểu hơn về cô gái, bạn mời cô ấy đi uống cafe nhưng tuần này thì thứ 5, tuần tới thứ 7, tuần nữa qua thứ 3, rồi bất chợt hai ngày liên tục ...v … để hiểu hơn về cô ấy nếu cuộc sống thay đổi như vậy thì cô ấy sẽ phản ứng thế nào.

Nhưng ngõ vào với nhiều sóng sine cùng biên độ thì cũng chỉ đủ để nhận dạng các hệ thống tuyến tính. Đối với các hệ thống phi tuyến, từng vùng làm việc khác nhau mối quan hệ giữa ngõ vào và ngõ ra cũng khác nhau nên để  extract càng nhiều đặc tính của hệ thống, các tính hiệu sóng sines ngõ vào cũng nên thay đổi biên độ. Kết quả là chúng ta có một tính hiệu ngõ vào lên xuống, thay đổi tần số khác nhau như white noise hay trong literature người ta còn gọi là pseudorandom binary sequence (PRBS). Cũng như muốn biết nhiều hơn về tính cách cô gái, không những phải thay đổi thời gian mời cô ấy đi uống cafe mà cần phải thay đổi cả nơi uống cafe (giá cả độ sang trọng khác nhau :-D). 

Tức là nghệ thuật của bước chuẩn bị dữ liệu ở chổ là làm sao kích thích hệ thống càng nhiều càng tốt để xem họ phản ứng thế nào. Càng có nhiều thông tin về hệ thống thì càng giúp cho quá trình nhận dạng tốt hơn. Nhưng nên nhớ đối với bạn gái các bạn cần phải đảm bảo ổn định, nếu để cô gái bất ổn (instable với bạn) là hỏng ngay. Trong topic này Lijung có nói closed-loop system identificaiton là ở chỗ đó. 

Bước 3: sau khi có được data thì nên chia data theo tỷ lệ 80-20, trong đó 80% dùng để đưa vào SysID toolbox và thuật toán tối ưu sẽ giúp nhận dạng các tham số của mô hình hệ thống; và 20% còn lại gọi là data tươi (fresh) để validate xem coi mô hình nhận dạng có fit với hệ thống không.

Tóm lại Phần 3 của cuốn sách Lijung muốn hướng dẫn người dùng làm sao thiết kế thí nghiệm để thu được data có ý nghĩa nhất cho việc nhận dạng hệ thống. Ngoài ra một phần quan trọng nữa là chọn cấu trúc mô hình, nhưng phần này thì cơ bản phương pháp là bắt đầu bằng cách chọn cấu trúc mô hình càng đơn giản (tuyến tính, ít bậc) càng tốt. Sau khi nhận dạng xong, validate với dữ liệu mới nếu thấy fit thì tốt, không thì có thể chọn mô hình khác (phi tuyến như Hammerstein, Winner) hoặc tăng bậc lên.

---

Như vậy về cơ bản ý nghĩa của cuốn sách Lijung là thế, khá nhiều toán nhưng cơ bản chúng ta có thể liên hệ system identification trong điều khiển và cuộc sống để hình dung nó dễ hơn, để dễ đọc hơn. Những nguyên tắc về mô hình hóa và nhận dạng hệ thống ở trên không chỉ quan trọng trong việc nhận dạng mô mình cho điều khiển mà nguyên lý của nó còn áp dụng cho việc thế kế các quỷ đạo cho các thiết bị không người lái, làm sao nó có thu được nhiều thông tin nhất về môi trường, về vật chuẩn để giúp nó định vị trong những điều kiện thông tin không được nhiều, và phần này liên quan đến một chủ đề quan trọng khác trong điều khiển gọi là "observability, detectability ... of dynamical systems". 
