---
title: 'The history of optimal control - Part II'
date: 2025-01-15
permalink: /posts/2020/11/proof-euler/
excerpt_separator: <!--more-->
usemath: true
tags:
  - Scientific story
  - Mathematic
  - Control 
---

# Điều Khiển Tối Ưu: Những dấu mốc trên con đường đã qua

## Phần 2: Quay ngược thời gian (trước 1950s)

Phần 1 điểm những dấu mốc lịch sử điều khiển tối ưu hiện đại bắt đầu từ 1950s, với những kết quả quan trọng như Pontryagin Maximum Principe (1957), sau đó là LQR của Kalman (1960). Điểm chung của PMP và LQR là đều dựa trên những kết quả trước đó của calculus of variation, ie. phương trình Hamilton. Vậy calculus of variation đến từ đâu và có gì thú vị, liệu có thể nhìn optimal control ở một lịch sử dài hơn không hay chỉ dừng lại ở thập niên 1950s?

<p align="center">
<img src="/images/posts/optimal_control/map_of_part_II.jpg" width="400">
</p>

Hector Saussan [1], trong bài báo kỷ niệm 300 năm ngày ra đời bài toán đường đi nhanh nhất (Brachistochrone), xuất bản 1997, cho rằng lịch sử optimal control có thể xem ra đời từ lúc Johhan Bernoulli giới thiệu bài toán này. Chuyện kể, năm 1696 trong ngày buồn “ko có việc gì làm”, Johhan “thách đố” các nhà toán lý vĩ đại nhất thời đó, với bài toán: giả sử có hai điểm A,B trên cùng một mặt phẳng đứng, dưới tác động duy nhất của trọng lực thì con đường nào khiến hòn bi lăn từ điểm A đến điểm B trong thời gian nhanh nhất. Sau đó cả thảy có 6 lời giải được công bố trong đó Leibniz (tháng 6, 1696), Newton (1697), mô tả rằng đường đi nhanh nhất không phải là đường thẳng mà là đường cong có dạng cycloid. Bài toán này chính là khởi đầu cho một lĩnh vực gọi là phương pháp biến phân (calculus of variantions), công cụ giải các bài toán liên quan tìm quỹ đạo tối ưu, và nền tảng cho lý thuyết điều khiển tối ưu sau này.

Trong các lời giải công bố thì của Jakob Bernoulli (anh trai của Johann Bernoulli) được xem là gần nhất cho sự phát triển sau này của calculus of variation, trong khi đó solution của Johan Bernoulli được xem là thú vị nhất. Johhan Bernoulli mượn nguyên lý Fermat (ánh sáng đi từ điểm A đến điểm B luôn theo đường có thời gian ngắn nhất) để giải, và để dễ hiểu ý tưởng của Bernoulli mọi người có thể xem thêm hình và giải thích đính kèm. Mình sau này học môn điều khiển tối ưu cũng có làm bài tập dùng nguyên lý Fermat để chứng minh định luật khúc xạ ánh sáng, và nhờ đó hiểu thêm về định luật này dù biết đến nó từ hồi phổ thông.
Bài toán đường đi nhanh nhất của Johan Bernoulli mở ra nghiên cứu về những bài toán tìm quỹ đạo tối ưu, khởi nguồn của sự ra đời calculus of variation. Một bước tiến lớn trong lĩnh vực này là nhờ đóng góp của Euler (học trò của Bernoulli). Chuyện kể là Euler vào học ĐH Basel từ năm 13 tuổi, và cứ hằng tuần Bernoulli nhồi cho một lecture riêng để giải bài toán tìm trajectory [x(t)] sao cho tối ưu (minimize/maximize) funtional:

J[x] = ∫ L(t, x, x') dt. (1)

Euler đưa ra được điều kiện tối ưu cho bài toán này nhưng phương pháp của ông được xem là không tổng quát, chủ yếu dựa vào hình học và cho từng bài toán cụ thể. Đến năm 1755, lúc đó Lagrance mới 19 tuổi gửi một bức thư cho Euler trình bày cách tiếp cận tổng quát và clean hơn nhờ dùng phương pháp biến phân (variation). Euler đã rất thích phương pháp này và dùng nó và kết quả cho ra đời phương trình điều kiện cần mang tên hai ông, Euler-Largrance (E-L):
d/dt (∂L/∂x') - ∂L/∂x = 0 (2)

Trong cơ học cơ học cổ điển (classical mechanics) nếu định nghĩa L(x,x_dot) = T - V, với x là hệ tọa độ (eg. vị trí, góc) của vật thể, T (động năng) và V (thế năng), chúng ta có thể áp dụng phương trình E-L để thu được hệ phương trình mô tả chuyển động vật thể giống như định luật Newton. Ưu điểm của Largrange mechanics so với Newton mechanics ở chổ là không cần phải phân tích lực, do đó có thể áp dụng tiện lợi hơn cho các hệ thống cơ học phức tạp.
Dấu mốc tiếp theo quan trọng trên con đến sự ra đời của optimal control hiện đại chính là công trình của Hamilton (1830s). Nghiên cứu của Hamilton ban đầu tập trung vào cơ học, giữ nguyên ý tưởng cơ học của Lagrange nhưng nhìn nhận chuyển động của vật chất ở gốc độ năng lượng. Ông giới thiệu hàm Hamilton có dạng

H(x, p, t) = p * x_dot - L(x, x_dot, t) (3)

trong đó: p được xem momentum (động lượng) và điều kiện cần cho quỷ đạo tối ưu thỏa mãn phương trình Halminton
dx/dt = ∂H/∂p và dp/dt = −∂H/∂x (4)
Về mặt cơ học, hàm Hamilton (3) thường có dạng tổng năng lượng của vật, tức là H = T + V, khác với hàm Lagrange ở chỗ L là chênh lệch giữa động năng (T) và thế năng (V). Điểm mạnh của phương pháp Halminon không chỉ nằm ở ứng dụng trong cơ học mà sau này còn được dùng trong quang học và lượng tử, tuy nhiên cá nhân mình chưa hiểu rõ hết những chủ đề này và cũng không liên quan đến nhiều optimal control nên xin không bàn ở đây.
Đến giữa thế kỷ 20, như chúng ta đã biết Pontryagin mở rộng phương pháp Hamilton, nhưng cho phép hệ thống được điều khiển bởi ngõ vào input (u) để đạt được một hàm tối ưu nào đó, thay vì trong cơ học cổ điển của Hamilton chỉ mô tả chuyển động của vật chất không có tác động bên ngoài. Và kết quả là như chúng ta đã biết đến nguyên lý Pontryagin ta biết ngày nay.
---

Như vậy điều khiển tối ưu tuy được xem ra đời từ những năm 50s của thế kỷ trước nhưng gốc gác của nó có thể nhìn về một lịch sử dài hơn đến tận cuối thế kỷ 17 khi Bernoulli giới thiệu bài toán đường đoản thời (Brachistochrone). Điều thú vị, không chỉ nằm ở vấn đề liên quan điều khiển, mà những kết quả từ calculus variation cho phép chúng ta hiểu và giải thích được rất nhiều hiện tượng tự nhiên, phải kể đến:
Định luật khúc xạ ánh sáng trên nguyên lý ánh sáng đi theo đường nhanh nhất
Đường cong chiếc võng (catenary) giải thích vật chất (không chuyển động) nghỉ ở trạng thái có thế năng nhỏ nhất
Vật trượt theo đường cong nhanh nhất (đường đoản thời Beunoulli (Cycloid))
Liệu có còn những hiện tượng tự nhiên nào có thể giải thích được với những kết quả của Euler, của Lagrange, hay Hamiton ? Và liệu những hiện tượng tự nhiên đó có thể giúp ích gì trong điều khiển ? Câu trả lời nằm ở những nhà điều khiển tài năng (trong nhóm chúng ta ?)
---

[1] HJ Sussmann (1997): 300 years of optimal control from the brachystochrone to the maximum principle
