---
title: 'Apply gyroscopic effect in attitude control of satellites'
date: 2023-12-15
permalink: /posts/2020/11/vu_con_quay/
excerpt_separator: <!--more-->
usemath: true
tags:
  - Scientific story
  - Mathematic
  - Control 
---
Đợt vừa rồi nhờ ứng dụng một effect vật lý (gọi là Gyroscopic effect) để điều khiển hướng vệ tinh và thấy thú vị nên xin chia sẻ cùng với mọi người ở đây.

<!--more-->
<p align="center">
<img src="/images/posts/vu_con_quay/vu_con_quay.jpg" width="900">
</p>

Để bắt đầu quay lại trò chơi vụ (con quay) mà chắc ai trong chúng ta cũng chơi hồi bé. Bọn nông thôn quê như mình gọi là vụ, nhưng một số nơi khác thì gọi là con quay. Hồi nhỏ bọn mình kiếm khúc gỗ mít, ổi, hay sầu đâu rồi đẽo thành hình con vụ. Nhớ không lầm gỗ ổi là chắc nhất, sau đó đến mít rồi đến sầu đâu. Mình kém khoản này nên toàn nhờ bạn làm hay đi xin rồi chơi.
Chơi trò này lúc đầu cả bọn giật dây cho nó xoay, cái của đứa nào đỗ xuống đất sớm nhất thì bị bỏ vào vòng tròn rồi những đứa khác nạp/nẻ lên đó nhằm mục tiêu phá hỏng con vụ của đối phương. Hồi đó cứ chơi nhưng cũng không thắc mắc vì sao mình phải giật manh cho nó quay nhanh để lâu đổ. Sau này có lần tìm hiểu thì đúng là không thể dễ giải thích chút nào.
Trong động học có khái niệm gọi là động lượng (momentum). Động lượng có hai loại, động lượng tịnh tiến (linear momentum) và động lượng quay (angular momentum). Động lượng tịnh tiến P = m*v còn động lượng quay L = J*w, trong đó m là khối lượng, v là vận tốc, J là moment quán tính còn w là vận tốc góc. Sức mạnh của một vật thể không phải chỉ dựa vào mỗi khối lượng mà chính xác là nằm ở động lượng của nó. Một viên đạn tuy nhỏ nhưng có sức mạnh ghê ghớm chính là nhờ nó có vận tốc cao, hay là động lượng cao.

Định luật 2 Newton đại khái nói rằng tốc độ thay đổi của động lượng phụ thuộc vào lực và moment (torque) bên ngoài tác động vào, i.e.

dP/dt = F_ext, và dL/dt = T_ext;

Điều này giúp mình giải thích hiện tượng con quay kể trên, đó là khi mình giật dây cho nó xoay thì mình cấp cho nó một động lượng quay khởi đầu L0. Dưới tác động của ma sát không khí và trọng lực trái đất angular momentum này dần bị tiêu hao (tức là L giảm đi) trong đó w giảm dần và hướng trục quay cũng thay đổi theo hướng đổ dần xuống đất. Khi đổ xuống, không quay nữa thì từ L0 → 0. Logic này cũng giải thích cho việc đi xe đạp hay xe gắn máy, nếu chúng ta chạy thì xe khó đổ còn dừng lại thì xe dễ đổ hơn.

Vậy những điều trên ứng dụng trong attitude control cho vệ tinh như thế nào ?

Đối với vệ tinh có một mode điều khiển liên quan attitude control là làm sao giữ hướng của các tấm pin mặt trời chiếu thẳng vào mặt trời trong một thời gian dài, mục tiêu là lấy được nhiều năng lượng mặt trời nhất. Điều này về mặt điều khiển thì không có gì khó khăn nếu dùng actuator đủ mạnh. Trong vệ tinh có 3 loại actuators phổ biến 1) thrusters 2) Reaction wheel và 3) magnetorquer. Loại đầu thì mạnh nhất nhưng tốn gas đốt nên không thể dùng lâu, do đó thường loại 2 hoặc 3 dùng cho mode này. Như bọn mình làm thì dùng loại thứ 3 nhưng vấn đề là loại thứ 3 rất yếu, có rất ít torque authority cho attitude control nên dẫn đến sai số rất lớn và mất thời gian rất lâu để stablize attitude control error.
Vậy là bọn mình dùng nguyên lý gyroscopic effect ở trên để hổ trợ attitude control. Ý tưởng là khởi đầu cho vệ tinh một angular momentum, đó là kích cho nó xoay quanh trục hướng đến mặt trời với một angular rate nào đó. và chính angular momentum khởi đầu này giúp chống lại sự thay đổi hướng của vệ tinh tác động bởi môi trường xung quanh. Việc còn lại là dùng một feedback control đơn giản kết hợp với magnetorquer để bù lại sự suy giảm của angular momentum kể trên gây ra bởi tác động của enviroment, qua đó giữ cho vệ tinh luôn hướng đến mặt trời như mong muốn.

Trong thời gian làm điều khiển cho các thiết bị xe cộ như thế này mình gặp và học được nhiều kỷ thuật như thế và thấy rằng nhiều lúc không phải lúc nào cũng có thể áp dụng control techniques vào ngay tức khắc mà việc hiểu rõ bản chất vật lý đằng sau đối tượng điều khiển là vô cùng quan trọng. Và nhiều lúc hết sức thú vị khi cùng một hiện tượng nhưng chúng ta không chỉ có thể nhìn nó từ góc nhìn điều khiển mà còn từ vật lý và khi kết hợp 2 hiểu biết này với nhau đưa ra những giải pháp vô cùng hiệu quả cho các bài toán engineering.