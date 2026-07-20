---
title: "Worklog Tuần 13"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.13. </b> "
---

### Mục tiêu tuần 13:

* Nghiên cứu chuyên sâu về các mô hình xử lý đồng thời (concurrency) nâng cao trong Kotlin, tập trung vào cơ chế hoạt động thực sự của Coroutines và Kotlin Flow.
* Làm chủ các khái niệm nâng cao trong Jetpack Compose, cụ thể là các giai đoạn render (rendering phases), tối ưu hóa hiệu năng và tự xây dựng các layout tùy chỉnh.
* Thiết kế kiến trúc phần mềm cho một ứng dụng Android quy mô lớn (scalable), ưu tiên hoạt động ngoại tuyến (offline-first) bằng cách áp dụng Clean Architecture, chia module (modularization) và kỹ thuật Dependency Injection nâng cao.
* Triển khai logic đồng bộ dữ liệu phức tạp và các animation giao diện nâng cao để mang lại trải nghiệm người dùng cao cấp nhất.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - **Xử lý đồng thời nâng cao với Kotlin (Concurrency & Flow):** <br>&emsp; + Phân tích sâu về Coroutine Context, Dispatchers và cơ chế hoạt động của Structured Concurrency <br>&emsp; + Làm chủ các toán tử Kotlin Flow (`flatMapLatest`, `combine`, `buffer`) và cách xử lý backpressure <br>&emsp; + Phân biệt và ứng dụng `StateFlow` vs `SharedFlow` cho việc quản lý state phức tạp và phát sự kiện (event broadcasting) <br>&emsp; + Viết unit test toàn diện cho các đoạn code Coroutine phụ thuộc vào thời gian bằng `runTest` và `TestCoroutineScheduler` | 13/07/2026   | 13/07/2026      | <https://developer.android.com/kotlin/coroutines/coroutines-adv> |
| 3   | - **Jetpack Compose nâng cao & Tối ưu hiệu năng:** <br>&emsp; + Tìm hiểu 3 giai đoạn của Compose: Composition, Layout, và Drawing <br>&emsp; + Tối ưu hóa render UI, hạn chế tối đa recomposition bằng cách sử dụng `remember`, `derivedStateOf` và immutable data classes <br>&emsp; + Xây dựng custom Modifiers và custom layout nâng cao bằng composable `Layout` và `SubcomposeLayout` <br>&emsp; + Xử lý các thao tác gesture phức tạp, drag-and-drop và hành vi nested scrolling | 14/07/2026   | 14/07/2026      | <https://developer.android.com/jetpack/compose/performance> |
| 4   | - **Clean Architecture & Multi-Module:** <br>&emsp; + Thiết kế project Android đa module (app, data, domain, core) để đảm bảo phân tách rõ ràng các tầng logic (separation of concerns) <br>&emsp; + Triển khai Dependency Injection bằng Dagger Hilt xuyên suốt nhiều module và quản lý vòng đời component phức tạp <br>&emsp; + Áp dụng luồng dữ liệu một chiều (Unidirectional Data Flow - UDF) với mẫu kiến trúc MVI (Model-View-Intent) <br>&emsp; + Định nghĩa các interface ranh giới nghiêm ngặt giữa tầng presentation, use cases và repository | 15/07/2026   | 15/07/2026      | <https://developer.android.com/topic/architecture>        |
| 5   | - **Kiến trúc Offline-First & Đồng bộ dữ liệu:** <br>&emsp; + Thiết kế lớp cache offline-first mạnh mẽ bằng Room Database với các mối quan hệ thực thể phức tạp (1:N, N:M) <br>&emsp; + Xử lý các kịch bản database migration trong Room và viết test tự động cho việc thay đổi schema <br>&emsp; + Triển khai thư viện Paging 3 với `RemoteMediator` để đồng bộ cache cục bộ với dữ liệu từ network một cách mượt mà <br>&emsp; + Giải quyết xung đột dữ liệu (data conflicts) giữa các thay đổi dưới local và bản cập nhật trên server | 16/07/2026   | 16/07/2026      | <https://developer.android.com/topic/architecture/data-layer/offline-first> |
| 6   | - **Animation nâng cao & Phân tích hiệu năng (Profiling):** <br>&emsp; + Xây dựng các animation tương tác, phức tạp bằng Compose Transition APIs (`updateTransition`, `AnimatedVisibility`, `animateContentSize`) <br>&emsp; + Vẽ custom graphics và biểu đồ dữ liệu trực tiếp lên Compose `Canvas` <br>&emsp; + Phân tích mức tiêu thụ CPU, RAM và Network bằng Android Studio Profiler và Macrobenchmark <br>&emsp; + Phát hiện và khắc phục lỗi rò rỉ bộ nhớ (memory leak) bằng LeakCanary và phân tích heap dump | 17/07/2026   | 17/07/2026      | <https://developer.android.com/studio/profile>            |

### Kết quả đạt được tuần 13:

* **Làm chủ Concurrency nâng cao trong Kotlin:** Đạt được sự hiểu biết sâu sắc về cách thức hoạt động nội tại của Kotlin Coroutines, khắc phục thành công các lỗi race conditions và triển khai các luồng dữ liệu phản ứng (reactive data streams) phức tạp bằng các toán tử Flow nâng cao.
* **Tối ưu hóa UI Rendering trong Compose:** Giảm thiểu đáng kể tình trạng giật lag (UI jank) và các vòng lặp recomposition không cần thiết trong Jetpack Compose bằng cách áp dụng kỹ thuật state hoisting nâng cao và custom modifiers, đạt được hiệu suất 60fps nhất quán trên các màn hình phức tạp.
* **Thiết kế kiến trúc Codebase khả mở (Scalable):** Tái cấu trúc thành công một ứng dụng nguyên khối (monolithic) thành cấu trúc Clean Architecture đa module. Sử dụng Dagger Hilt để tiêm phụ thuộc (dependency injection) mạnh mẽ, đảm bảo sự cô lập tuyệt đối giữa tầng domain và tầng data.
* **Triển khai trải nghiệm Offline-First liền mạch:** Chế tạo một hệ thống lưu trữ đệm (local caching) có khả năng chống chịu lỗi cao với Room và Paging 3 `RemoteMediator`. Ứng dụng có thể hoạt động hoàn hảo ngay cả khi mất mạng hoàn toàn và âm thầm đồng bộ dữ liệu chênh lệch (deltas) ở chế độ nền ngay khi có kết nối trở lại.
* **Mang lại trải nghiệm UX cao cấp & Ổn định tuyệt đối:** Nâng tầm tính thẩm mỹ và chất lượng tương tác của ứng dụng bằng cách tự vẽ các thành phần đồ họa Canvas độ tùy biến cao và các hiệu ứng chuyển động mượt mà, dựa trên vật lý (physics-based). Khắc phục triệt để lỗi rò rỉ bộ nhớ và cải thiện băng thông tổng thể thông qua quá trình phân tích (profiling) và tối ưu hóa khắt khe.
