---
title: 'Control techniques in satellites and rocket launching vehicles'
date: 2023-09-15
permalink: /posts/2020/11/Control techniques in satellites and rocket launching vehicles/
excerpt_separator: <!--more-->
usemath: true
tags:
  - Scientific story
  - Mathematic
  - Control 
---

Khi có cơ hội về lại trường củ, hoặc đi các events gặp đồng nghiệp mình hay giới thiệu về các dự án điều khiển bọn mình đang làm cho các thiết bị trong không gian và mọi người hay thắc mắc là kỷ thuật điều khiển ngành này hay dùng là gì, và khi trao đổi có nhiều thứ rất thú vị.
<!--more-->
Có lẻ mọi người sẽ rất ngạc nhiên khi được biết rằng kỷ thuật điều khiển cho tên lửa, vệ tinh, những cỗ máy vô cùng phức tạp, lại rất đơn giản, chủ yếu PID, LQR, hoặc PID kết hợp thêm với các state feedback khác. Gần đây thì có thêm Hinf, và đang dần trở thành sự lựa chọn mặc định trong các dự án liên quan đến space industry ở EU. Vậy tại sao bao nhiêu năm qua, với sự ra đời rất nhiều “advanced” non-linear techniques khác, từ Fuzzy, Sliding Mode, MPC, cho đến AI-based như RL, vv nhưng linear control đơn giản kể trên vẫn phổ biết trong space industry ? Có lẽ do những nguyên nhân sau.

- Đơn giản
- Tin cậy
- Đã được chứng minh thành công

1. Nguyên nhân thứ nhất chắc ai cũng thấy. PID, LQR, hay thậm chí Full order Hinf cơ bản vẫn rất đơn giản so với các thuật toán phi tuyến khác kể trên. Đơn giản ở đây không chỉ là trong thiết kế, mà cả phân tích stability, và trong implementation. Cái sau vô cùng quan trọng nếu chúng ta biết rằng thời gian tính toán cho toàn bộ hệ thống guidance, navigation, and control cho một tên lửa đây bọn mình đang làm cho công ty Orbex [1] chỉ là 2ms.

2. Về cơ bản lý thuyết điều khiển tuyến tính có thể nói đã rất hoàn chỉnh, và có rất nhiều công cụ tin cậy cho việc phân tính tính ổn định, từ time domain, frequency domain, cho đến ảnh hưởng của model uncertainty. Phân tích và thiết kế bộ điều khiển trong frequency domain cho space vehicles cực kỳ quan trọng bởi trong quá trình thiết kế phải xác định rõ đâu là bandwidths của controllers, của actuators, của các filters để làm sao đảm bảo bộ điều khiển vừa track được reference signals, nhưng lại loại bỏ được các ảnh hưởng của sloshing (i.e. dao động của nhiên liệu lỏng tác động lên vehicle), hoặc bending modes ( eg. trong trường hợp tên lửa bị uốn cong, hoặc khi các solar panel bị biến dạng trong các ứng dụng sattlite) …, vv. Ngoài ra Mui analysis, cho phép phân tích tính ổn định không chỉ cho nominal mà còn cho dispersion của model parameters mà theo hiểu biết của mình không dễ làm nếu dùng điều khiển phi tuyến.

3. Và cuối cùng, sở dĩ các phương pháp điều khiển đơn giản như PID được chọn cho đến ngày bởi vì nó đã chứng minh được hiệu quả trong các chuyến bay thực tế. Nếu trong robotics (indoor, ground, hoặc marine) nếu chúng ta thử một bộ điều khiển mới, không chạy chúng ta có thể thử lại, nhưng đối với tên lửa đẩy chẳng hạn, nếu sai thì có thể đi cả chục, thậm chí đến trăm triệu đô thì cơ bản thấy rằng cái nào đã worked thì cố gắng làm theo là xong 🙂.

Chia sẻ ở đây để thấy rằng vai trò của điều khiển tuyến tính vẫn rất quan trọng, nhất là trong aerospace industry. Thậm chí European Space Agency có hẳn bộ quy chuẩn hướng dẫn bộ điều khiển phải có phase margin, gain margins, peaks of sensitivity là bao nhiêu để các công ty thiết kế follow.

<!--more-->
<p align="center">
<img src="/images/posts/dieu_khien_ve_tinh/clear_space_sattlite.jpg" width="400">
</p>

<!--more-->
<p align="center">
<img src="/images/posts/dieu_khien_ve_tinh/orbex_rocket.jpg" width="400">
</p>


Hai hình đính kèm liên quan đến 2 project trong space industry ở EU mà mình tham gia và đóng góp 2 năm qua và thiết kế toàn bộ hệ thống điều khiển cho nó cho đến bây giờ.

- H1: Launching vehicles của Orbex (UK) https://orbex.space/ và
- H2: Spacecraft của ClearSpace (Switzerland), https://clearspace.today/