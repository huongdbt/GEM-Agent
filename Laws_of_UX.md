# Laws of UX — Bộ Luật Thiết Kế Trải Nghiệm Người Dùng
**Nguồn:** lawsofux.com — tổng hợp bởi Jon Yablonski
**License:** Creative Commons BY-NC-ND 4.0
**Mục đích file:** Tài liệu tham khảo cho Gem UX Research Lab — dùng kết hợp với UX_Patterns.md và UIUX_Combined_for_Gem.md

---

## Tổng quan — 30 Luật theo nhóm

| Nhóm | Luật |
|------|------|
| **Nhận thức & Tri giác** | Aesthetic-Usability Effect, Law of Proximity, Law of Similarity, Law of Common Region, Law of Prägnanz, Law of Uniform Connectedness, Von Restorff Effect, Serial Position Effect, Selective Attention |
| **Bộ nhớ & Xử lý thông tin** | Miller's Law, Chunking, Working Memory, Cognitive Load, Cognitive Bias, Mental Model, Zeigarnik Effect |
| **Quyết định & Lựa chọn** | Hick's Law, Choice Overload, Occam's Razor, Pareto Principle, Tesler's Law |
| **Hành vi & Động lực** | Goal-Gradient Effect, Peak-End Rule, Fogg Behavior Model, Paradox of the Active User, Parkinson's Law |
| **Hiệu năng & Tương tác** | Fitts's Law, Doherty Threshold, Postel's Law, Flow, Jakob's Law |

---

# NHÓM 1: NHẬN THỨC & TRI GIÁC

---

## 01. Aesthetic-Usability Effect
**Định nghĩa:** Người dùng thường nhận thức thiết kế đẹp như là thiết kế dễ dùng hơn.

**Tại sao nó hoạt động:**
Não bộ liên kết vẻ đẹp với chất lượng. Thiết kế đẹp tạo cảm giác tích cực, làm tăng khả năng chịu đựng lỗi nhỏ và giảm cảm giác khó khăn khi dùng sản phẩm.

**Ứng dụng vào thiết kế:**
- Đầu tư vào visual polish trước khi launch — thiết kế đẹp giúp user bỏ qua friction nhỏ
- Sản phẩm có UI đẹp được đánh giá dễ dùng hơn dù khó dùng thực sự
- Cẩn thận: Đừng che giấu usability issues bằng aesthetics — người dùng cuối cũng sẽ phát hiện ra
- Đặc biệt quan trọng với impression đầu tiên: 7 giây đầu quyết định perception

**Ví dụ thực tế:**
- Apple: Thiết kế premium → user cảm thấy thiết bị "mượt hơn" dù hiệu suất tương đương
- Linear: Dark mode đẹp → developer cảm thấy tool "nhanh và chính xác hơn"

**Liên quan đến:** Law of Prägnanz, Flow State

---

## 02. Law of Proximity
**Định nghĩa:** Các đối tượng gần nhau có xu hướng được nhóm lại với nhau.

**Tại sao nó hoạt động:**
Gestalt psychology — não tự động nhóm các phần tử gần nhau thành một đơn vị ý nghĩa mà không cần viền hay màu sắc phân biệt.

**Ứng dụng vào thiết kế:**
- Label của input field phải gần input hơn là gần field phía trên
- Related actions (Edit, Delete) nên nhóm lại, cách biệt với actions khác
- Card layout: tiêu đề + mô tả + CTA phải gần nhau hơn là cách biệt
- Spacing có ý nghĩa: khoảng cách lớn = ranh giới nhóm; khoảng cách nhỏ = cùng nhóm

**Ví dụ thực tế:**
- Form design: "Họ" và "Tên" gần nhau → nhóm thông tin cá nhân; sau đó khoảng cách lớn trước "Địa chỉ"
- Notion sidebar: Pages con thụt vào gần page cha

---

## 03. Law of Similarity
**Định nghĩa:** Mắt người có xu hướng nhận thức các phần tử giống nhau là một nhóm hoàn chỉnh, dù chúng cách biệt nhau.

**Tại sao nó hoạt động:**
Não tìm pattern và group dựa trên hình dạng, màu sắc, kích thước tương đồng — cần ít công sức nhận thức hơn.

**Ứng dụng vào thiết kế:**
- Các interactive elements (links, buttons) nên trông giống nhau để dễ nhận diện
- Navigation items có cùng font/color → user hiểu đây là "cùng cấp"
- Dùng màu để phân nhóm: tất cả lỗi màu đỏ, tất cả thành công màu xanh
- Phá similarity có chủ đích để highlight item đặc biệt (Von Restorff Effect)

**Ví dụ thực tế:**
- Spotify: Tất cả track items trông giống nhau → user hiểu đây là list có thể tương tác
- Linear: Tất cả issue items có cùng structure → dễ scan

---

## 04. Law of Common Region
**Định nghĩa:** Các phần tử trong cùng một vùng có ranh giới rõ ràng có xu hướng được nhận thức là nhóm.

**Ứng dụng vào thiết kế:**
- Card components tạo ranh giới tự nhiên cho nhóm thông tin liên quan
- Dùng background color khác để phân vùng (header, sidebar, footer)
- Groupbox / panel tạo context cho các controls bên trong
- Đặc biệt hữu ích khi các items không gần nhau về vị trí (Common Region bù cho Proximity)

---

## 05. Law of Prägnanz (Law of Good Form)
**Định nghĩa:** Người dùng sẽ nhận thức và diễn giải hình ảnh mơ hồ hoặc phức tạp theo dạng đơn giản nhất có thể, vì đó là cách đòi hỏi ít công sức nhận thức nhất.

**Ứng dụng vào thiết kế:**
- Thiết kế icon đơn giản, rõ nghĩa hơn là phức tạp và chi tiết
- Khi muốn user hiểu hierarchy, dùng hình dạng đơn giản và rõ ràng
- Logo và brand mark: đơn giản → nhớ lâu hơn, nhận ra nhanh hơn
- Loaders, progress indicators: hình tròn/thanh đơn giản beats complex animation cho clarity

---

## 06. Law of Uniform Connectedness
**Định nghĩa:** Các phần tử được kết nối bằng đường hoặc vùng đồng nhất được nhận thức là liên quan đến nhau hơn các phần tử không có kết nối.

**Ứng dụng vào thiết kế:**
- Progress steps: kết nối bằng đường → user thấy đây là một sequence
- Breadcrumb: dấu `/` hay `>` kết nối các level
- Timeline: đường dọc kết nối các events → nhìn ngay là chronological
- Khi muốn nhấn mạnh 2 items KHÔNG liên quan: loại bỏ các kết nối và tạo khoảng cách rõ ràng

---

## 07. Von Restorff Effect (Isolation Effect)
**Định nghĩa:** Khi có nhiều vật tương tự xuất hiện cùng nhau, vật khác biệt với các vật còn lại sẽ được nhớ nhiều nhất.

**Ứng dụng vào thiết kế:**
- "Recommended" plan trong bảng giá: màu khác / size lớn hơn / highlight border
- CTA button phải contrast với surrounding elements → dễ nhìn thấy
- Warning/Error messages: màu đỏ trong giao diện neutral → thu hút ngay lập tức
- Dùng có chủ đích: chỉ 1 phần tử khác biệt mới tạo hiệu ứng; quá nhiều = không có gì nổi bật
- Đừng overuse: nếu mọi thứ đều highlighted, không có gì được highlight

**Ví dụ thực tế:**
- Stripe pricing: "Most popular" plan có background đặc biệt
- Duolingo: Streak flame màu cam nổi bật trong giao diện xanh lá

---

## 08. Serial Position Effect
**Định nghĩa:** Người dùng có xu hướng nhớ tốt nhất item đầu tiên (Primacy Effect) và item cuối cùng (Recency Effect) trong một series.

**Ứng dụng vào thiết kế:**
- **Navigation:** Đặt items quan trọng nhất ở đầu hoặc cuối list, không ở giữa
- **Onboarding steps:** Step đầu và step cuối tạo ấn tượng mạnh nhất — đầu tư vào 2 điểm này
- **Pricing table:** Plan quan trọng nhất nên ở vị trí đầu hoặc cuối, không giữa
- **Email subject line:** Từ đầu và từ cuối được nhớ nhiều hơn — đặt keyword quan trọng ở 2 đầu
- **Feature list:** Limit ở 5-7 items; nếu dài hơn, user chỉ nhớ đầu và cuối

**Liên quan đến:** Miller's Law, Working Memory

---

## 09. Selective Attention
**Định nghĩa:** Quá trình chỉ tập trung vào một phần nhỏ các kích thích trong môi trường — thường là những kích thích liên quan đến mục tiêu của chúng ta.

**Ứng dụng vào thiết kế:**
- User đang tìm kiếm thứ gì đó sẽ bỏ qua mọi thứ không liên quan (kể cả ads)
- "Banner blindness": Người dùng tự động ignore vùng trông giống quảng cáo
- Đặt thông tin quan trọng trong vùng user đang nhìn (trong task flow, không ở sidebar)
- Giảm distraction: Remove bất kỳ thứ gì không phục vụ mục tiêu hiện tại của user
- Notifications: Chỉ hiện khi liên quan đến task user đang làm

---

# NHÓM 2: BỘ NHỚ & XỬ LÝ THÔNG TIN

---

## 10. Miller's Law
**Định nghĩa:** Người bình thường chỉ giữ được 7 (±2) items trong working memory cùng lúc.

**Ứng dụng vào thiết kế:**
- Navigation: Không quá 7 items ở top level
- Feature list trên landing page: Giới hạn 5-7 key benefits
- Form: Chia thành nhiều bước nếu tổng có hơn 7 fields
- Dashboard: Không hiện hơn 7 metrics cùng lúc — nhóm và ẩn bớt
- Menu dropdown: Không quá 7 options; thêm section headers nếu cần nhiều hơn

**Lưu ý quan trọng:**
"7±2" là số items riêng lẻ. Chunking (nhóm lại) có thể tăng effective capacity — đây là tại sao mã số điện thoại được chia nhóm (0123 456 789 dễ nhớ hơn 0123456789).

---

## 11. Chunking
**Định nghĩa:** Quá trình chia nhỏ thông tin thành các phần và nhóm lại thành một tổng thể có ý nghĩa.

**Ứng dụng vào thiết kế:**
- Số điện thoại: `0901 234 567` thay vì `0901234567`
- Credit card: `4532 1234 5678 9012` chia thành 4 nhóm
- Dashboard metrics: Nhóm theo chủ đề (Revenue metrics / Engagement metrics / Retention metrics)
- Long-form content: Chia thành sections với headers rõ ràng
- Onboarding steps: Nhóm các bước liên quan ("Setup your profile" gồm 3 sub-steps)

**Liên quan đến:** Miller's Law, Cognitive Load

---

## 12. Working Memory
**Định nghĩa:** Hệ thống nhận thức tạm thời giữ và xử lý thông tin cần thiết để hoàn thành các nhiệm vụ.

**Ứng dụng vào thiết kế:**
- Recognition beats recall: Show options, don't make users remember (dropdown vs text input)
- Breadcrumbs: Giúp user không phải nhớ họ đang ở đâu trong hierarchy
- Keep context visible: User đang làm gì, đã làm gì, sẽ làm gì tiếp — luôn visible
- Đừng yêu cầu user nhớ thông tin từ màn hình trước để điền vào màn hình sau
- Search: Show recent searches — user không phải nhớ lại những gì đã tìm

---

## 13. Cognitive Load
**Định nghĩa:** Lượng tài nguyên tâm thần cần thiết để hiểu và tương tác với một giao diện.

**3 loại Cognitive Load:**
- **Intrinsic:** Độ phức tạp cố hữu của task (không thể loại bỏ)
- **Extraneous:** Độ phức tạp do thiết kế kém (phải loại bỏ)
- **Germane:** Công sức xây dựng mental model (nên hỗ trợ tốt)

**Ứng dụng vào thiết kế:**
- Loại bỏ Extraneous Load: Bỏ decorative elements không có chức năng, clarify unclear labels
- Giảm Intrinsic Load: Progressive disclosure, chia task phức tạp thành steps nhỏ
- Hỗ trợ Germane Load: Onboarding tốt giúp user build mental model chính xác nhanh hơn
- Inline help và tooltips giảm cognitive load cho feature phức tạp

---

## 14. Cognitive Bias
**Định nghĩa:** Lỗi hệ thống trong tư duy hoặc phán đoán ảnh hưởng đến nhận thức và khả năng quyết định.

**Các bias quan trọng nhất trong UX:**
- **Confirmation Bias:** Người dùng tìm thông tin xác nhận niềm tin sẵn có → thiết kế để không bị exploit
- **Anchoring Bias:** Giá đầu tiên xem ảnh hưởng đến đánh giá giá sau → pricing strategy
- **Status Quo Bias:** Prefer giữ nguyên hiện trạng → đặt deault options một cách cẩn thận
- **The Bandwagon Effect:** Làm theo số đông → social proof design
- **Framing Effect:** Cùng một thông tin được frame khác nhau dẫn đến quyết định khác → copy writing

**Ứng dụng vào thiết kế:**
- Đặt default options có chủ đích (Status Quo Bias — user giữ default)
- Dùng anchoring: Hiện "giá gốc" trước "giá sau giảm"
- Thiết kế để không manipulate — dùng bias một cách đạo đức, không phải exploit

---

## 15. Mental Model
**Định nghĩa:** Mô hình thu gọn dựa trên những gì chúng ta nghĩ mình biết về một hệ thống và cách nó hoạt động.

**Ứng dụng vào thiết kế:**
- Thiết kế phải match mental model của user, không phải của developer
- "Save" icon = floppy disk: user vẫn hiểu dù không bao giờ dùng đĩa mềm
- Khi thay đổi UX pattern đã quen → cần thêm thời gian và explanation cho user
- User research để hiểu mental model của target user trước khi thiết kế
- Jakob's Law: Mental model từ app khác được transfer sang app của bạn

**Liên quan đến:** Jakob's Law, Paradox of the Active User

---

## 16. Zeigarnik Effect
**Định nghĩa:** Người ta nhớ các tasks chưa hoàn thành hoặc bị gián đoạn tốt hơn các tasks đã hoàn thành.

**Ứng dụng vào thiết kế:**
- Progress bars và completion percentages tạo tension muốn complete
- "Profile 60% complete" makes user want to finish
- Save draft / "Continue where you left off" giữ user quay lại
- Tạo micro "open loops" trong onboarding: "Step 1 ✓ — Step 2 pending" → motivation to continue
- Cliffhangers trong content (articles, courses): end at a question, not an answer

**Liên quan đến:** Goal-Gradient Effect, Progress Visibility Pattern

---

# NHÓM 3: QUYẾT ĐỊNH & LỰA CHỌN

---

## 17. Hick's Law
**Định nghĩa:** Thời gian để đưa ra quyết định tăng dần theo số lượng và độ phức tạp của các lựa chọn.

**Công thức:** T = b × log₂(n + 1) — Thời gian phản hồi = hằng số × log số lựa chọn

**Ứng dụng vào thiết kế:**
- Navigation: Giới hạn số lượng menu items ở top level (5-7)
- Pricing page: 3 tiers là optimal; 5+ gây paralysis
- Onboarding: Đưa ra từng quyết định một, không cùng lúc nhiều quyết định
- Remote controls, dashboards: Chỉ hiện controls cần thiết tại thời điểm đó
- Search kết quả: Pagination / infinite scroll để không overload bằng 1000 results cùng lúc

**Áp dụng có chọn lọc:**
- Hick's Law không áp dụng cho cases người dùng đang tìm kiếm một item cụ thể trong list dài (search task khác với decision task)

---

## 18. Choice Overload
**Định nghĩa:** Xu hướng người dùng bị choáng ngợp khi phải đối mặt với quá nhiều lựa chọn — thường dùng thay thế cho "paradox of choice".

**Nghiên cứu nền tảng:**
Iyengar & Lepper (2000): Jam study — 24 loại jam vs 6 loại jam. 6 loại bán được nhiều hơn 10 lần dù có ít lựa chọn hơn.

**Ứng dụng vào thiết kế:**
- Catalog lớn: Dùng filters + personalization để giảm effective choices
- "Recommended for you" / "Editor's choice" → pre-selects tốt nhất → giảm overload
- Onboarding: Cho user chọn 1 "path" (cá nhân/doanh nghiệp, beginner/expert) → customize experience
- Ecommerce: Hiện "bestseller" / "top rated" trước khi user filter
- Giảm options ở checkout: Amazon "1-Click" là extreme version — loại bỏ mọi lựa chọn

---

## 19. Occam's Razor
**Định nghĩa:** Trong các giả thuyết giải thích tương đương, giả thuyết đơn giản nhất (ít giả định nhất) nên được chọn.

**Ứng dụng vào thiết kế:**
- Khi có 2 design solutions giải quyết cùng một vấn đề → chọn cái đơn giản hơn
- Feature creep: Mỗi feature mới phải có justification — "thêm vào" có cost ẩn
- UI: Loại bỏ bất kỳ element nào không phục vụ mục đích rõ ràng
- Copy: Câu ngắn hơn, rõ nghĩa hơn luôn tốt hơn câu dài phức tạp
- Architecture: Đơn giản nhất có thể, nhưng không đơn giản hơn mức cần (Einstein)

---

## 20. Pareto Principle (80/20 Rule)
**Định nghĩa:** 80% kết quả đến từ 20% nguyên nhân.

**Ứng dụng vào thiết kế:**
- 80% người dùng dùng 20% features → tập trung vào 20% đó
- 80% revenue đến từ 20% user segments → cá nhân hóa cho segment đó
- 80% bugs đến từ 20% code → ưu tiên fix theo impact
- Navigation: 20% destinations chiếm 80% clicks → đặt chúng ở vị trí nổi bật nhất
- UX Research: 5 user interviews thường phát hiện 85% usability issues

---

## 21. Tesler's Law (Law of Conservation of Complexity)
**Định nghĩa:** Trong mọi hệ thống có một mức độ phức tạp nhất định không thể giảm bớt.

**Ứng dụng vào thiết kế:**
- Phức tạp không biến mất — nó chỉ được chuyển từ user sang system (hoặc ngược lại)
- Designer giỏi: Nhận complexity từ user và xử lý nó trong system/backend
- Designer kém: Để user tự xử lý complexity
- Ví dụ: Email client "undo send" — xử lý complexity của việc gửi nhầm thay vì để user cẩn thận hơn
- Smart defaults: Thay vì user configure mọi thứ, system tự chọn default hợp lý

**Ranh giới quan trọng:**
Đừng oversimplify đến mức mất flexibility. Power users cần access đến complexity không thể loại bỏ.

---

# NHÓM 4: HÀNH VI & ĐỘNG LỰC

---

## 22. Goal-Gradient Effect
**Định nghĩa:** Xu hướng nỗ lực tiếp cận mục tiêu tăng lên khi gần đến đích.

**Nghiên cứu nền tảng:**
Rats chạy nhanh hơn khi gần hộp thức ăn. Khách hàng mua hàng thường xuyên hơn khi gần đủ điểm để đổi phần thưởng.

**Ứng dụng vào thiết kế:**
- Progress bars: Đặc biệt hiệu quả khi gần 100% → accelerate action
- "Boosted start" technique: Cho user 20% progress trước khi bắt đầu (như đã có điểm sẵn)
- Loyalty programs: Cho user "head start" points khi signup → engagement cao hơn từ đầu
- Onboarding: Ngay khi đăng ký, hiện "Profile 30% complete" → tạo gap cần fill
- Countdown: "Hoàn thành 1 task nữa để mở khóa..." → tăng urgency gần đích

**Liên quan đến:** Zeigarnik Effect, Progress Visibility Pattern

---

## 23. Peak-End Rule
**Định nghĩa:** Người dùng đánh giá trải nghiệm chủ yếu dựa trên cảm xúc tại đỉnh (peak) và lúc kết thúc (end), không phải trung bình tổng thể.

**Nghiên cứu nền tảng:**
Kahneman et al.: Bệnh nhân colonoscopy — thêm vài giây nhẹ nhàng ở cuối khiến trải nghiệm được nhớ dễ chịu hơn dù tổng thời gian dài hơn.

**Ứng dụng vào thiết kế:**
- **Peak**: Thiết kế moments thỏa mãn cực điểm (wow moments) — Aha Moment, first success
- **End**: Đặc biệt chú ý đến experience kết thúc — completion animation, success message, "what next"
- Onboarding: End of onboarding phải memorable và satisfying
- Checkout: "Thank you" page / Order confirmation là "end" → đừng để nó là blank
- Error recovery: Nếu pipeline có error, recovery experience phải feel good → ảnh hưởng memory của toàn bộ session

---

## 24. Paradox of the Active User
**Định nghĩa:** Người dùng không đọc manual mà bắt đầu dùng phần mềm ngay lập tức.

**Tại sao nó xảy ra:**
Người dùng rational biết đọc manual sẽ giúp họ nhanh hơn, nhưng bắt đầu làm ngay cảm giác có productive hơn. Paradox: Cách kém hiệu quả cảm giác hiệu quả hơn.

**Ứng dụng vào thiết kế:**
- Đừng dựa vào manual hay onboarding tour — user sẽ bỏ qua
- Thiết kế để discoverable: Feature phải tự giải thích được mà không cần documentation
- Progressive disclosure: Contextual help khi user cần, không phải upfront
- Tooltips on hover và inline guidance thay vì welcome modal
- Empty states là phần documentation duy nhất user thực sự đọc

---

## 25. Parkinson's Law
**Định nghĩa:** Mọi task sẽ mở rộng để lấp đầy toàn bộ thời gian được phân bổ cho nó.

**Ứng dụng vào thiết kế:**
- **Deadline trong design**: Tạo time pressure hợp lý → focus, tránh scope creep
- **Form completion**: Hiển thị "estimated time: 3 minutes" → user commit finish
- **Checkout**: Multi-step checkout với progress indicator → user biết endpoint, không dần lười
- **Onboarding**: Giới hạn rõ ràng số steps → không để onboarding "bò" thêm
- **For designers**: Set artificial deadlines cho design review → tránh endless iteration

---

# NHÓM 5: HIỆU NĂNG & TƯƠNG TÁC

---

## 26. Fitts's Law
**Định nghĩa:** Thời gian để chạm vào một target là hàm số của khoảng cách đến target và kích thước của target.

**Công thức:** T = a + b × log₂(D/W + 1)
- T = thời gian; D = khoảng cách; W = kích thước target

**Ứng dụng vào thiết kế:**
- **Touch targets:** Minimum 44×44px (Apple) / 48×48dp (Google) cho mọi tappable element
- **Primary CTAs:** Đặt ở vùng dễ reach nhất (bottom on mobile, không phải top)
- **Pie menus:** Targets theo vòng tròn — mọi option cùng khoảng cách (better than linear dropdown)
- **Destructive actions** (Delete): Nhỏ hơn và xa hơn CTA chính → giảm accidental tap
- **Desktop:** Edges và corners màn hình có effective size vô hạn → macOS dock, Windows Start button
- **Spacing between targets:** Tăng gap giữa các buttons liền kề để tránh miss-tap

---

## 27. Doherty Threshold
**Định nghĩa:** Năng suất tăng vọt khi máy tính và người dùng tương tác ở tốc độ dưới 400ms — đảm bảo không bên nào phải chờ.

**Ứng dụng vào thiết kế:**
- **Target:** <100ms cho feedback tức thì; <400ms cho response cảm giác "tức thì"
- **1000ms+**: User bắt đầu mất focus và chuyển sang task khác
- **Loading states:** Hiện progress indicator sau 400ms để user biết system đang làm gì
- **Skeleton screens** tốt hơn spinners: User thấy content structure → feel faster
- **Optimistic UI:** Update UI ngay lập tức, xử lý backend sau → feel instant
- **Animation duration:** UI animations nên <300ms — nhanh = modern / chuyên nghiệp

---

## 28. Postel's Law (Robustness Principle)
**Định nghĩa:** Hãy chấp nhận rộng rãi những gì nhận được, và gửi đi một cách bảo thủ.

**Nguyên bản:** TCP/IP design principle của Jon Postel — "Be conservative in what you do, be liberal in what you accept from others."

**Ứng dụng vào thiết kế:**
- **Form inputs:** Accept nhiều format: điện thoại với hoặc không dấu `-`, `()`, khoảng trắng
- **Input flexibility:** Accept `john@email.com` và `John@Email.COM` như nhau
- **Date input:** Accept nhiều format date (MM/DD/YYYY và DD/MM/YYYY)
- **Search:** Fuzzy matching, typo tolerance, synonym handling
- **Output:** Data output của bạn phải consistent, predictable, và đúng format
- **Error messages:** Đừng reject và yêu cầu exact format khi intention rõ ràng

---

## 29. Flow State
**Định nghĩa:** Trạng thái tâm lý khi người thực hiện một hoạt động hoàn toàn đắm chìm trong cảm giác tập trung đầy năng lượng, toàn tâm toàn ý, và hứng thú với quá trình.

**Điều kiện để đạt Flow (Csikszentmihalyi):**
- Challenge ≈ Skill: Quá dễ = chán; Quá khó = frustrated; Vừa sức = Flow
- Clear goals và immediate feedback
- Không bị ngắt quãng

**Ứng dụng vào thiết kế:**
- Loại bỏ mọi interruption trong task stream (unexpected modals, unrelated notifications)
- Thiết kế feedback loops: Mỗi action có response ngay lập tức
- Progressive complexity: Features mới mở ra sau khi user master features cơ bản
- "Focus mode" trong productivity tools: Hide distractions → enable flow
- Gaming: Level design tăng dần đều = classic flow design

---

## 30. Jakob's Law
**Định nghĩa:** Người dùng dành phần lớn thời gian trên các sản phẩm khác. Điều này có nghĩa là họ muốn ứng dụng của bạn hoạt động giống như tất cả các ứng dụng khác họ đã biết.

**Ứng dụng vào thiết kế:**
- Tuân theo platform conventions (iOS Human Interface Guidelines, Android Material Design)
- Shopping cart icon = giỏ hàng; không cần phát minh lại icon mới
- Hamburger menu (☰): Dù bị chỉ trích, user đã quen → không cần alternative phức tạp
- Đừng sáng tạo với interaction patterns cơ bản (scroll direction, swipe to go back)
- Khi muốn phá convention: cần cost-benefit analysis — innovation cost vs Jakob's Law benefit
- B2B SaaS: Nếu users đến từ Excel/Google Sheets, imitate spreadsheet paradigm

**Ranh giới:**
Jakob's Law tốt cho foundation; nhưng differentiation đến từ việc làm tốt hơn, không phải khác biệt hơn.

---

# QUICK REFERENCE TABLE — TẤT CẢ 30 LUẬT

| # | Luật | Một câu tóm tắt | Áp dụng chính |
|---|------|-----------------|---------------|
| 01 | Aesthetic-Usability Effect | Đẹp → cảm giác dễ dùng | Visual polish quan trọng ngay cả với usability |
| 02 | Law of Proximity | Gần = cùng nhóm | Spacing có ý nghĩa, không phải decoration |
| 03 | Law of Similarity | Giống nhau = cùng nhóm | Consistency trong style cho related elements |
| 04 | Law of Common Region | Cùng vùng = cùng nhóm | Cards, borders, background color tạo nhóm |
| 05 | Law of Prägnanz | Não chọn hình dạng đơn giản nhất | Đơn giản hóa icon, UI, mental model |
| 06 | Law of Uniform Connectedness | Nối nhau = liên quan | Lines, flows, breadcrumbs tạo sequence |
| 07 | Von Restorff Effect | Khác biệt → nhớ hơn | Highlight CTA, warning, featured item |
| 08 | Serial Position Effect | Nhớ đầu và cuối tốt nhất | Nav và list: important items đầu/cuối |
| 09 | Selective Attention | User chỉ thấy những gì liên quan mục tiêu | Đặt key info trong task flow, không ở sidebar |
| 10 | Miller's Law | 7±2 items trong working memory | Max 7 nav items, form fields, menu options |
| 11 | Chunking | Nhóm thông tin thành đơn vị có nghĩa | Breaking up phone numbers, steps, sections |
| 12 | Working Memory | Bộ nhớ tạm thời giữ context | Recognition over recall, breadcrumbs |
| 13 | Cognitive Load | Tải nhận thức cần minimize | Progressive disclosure, clear labels |
| 14 | Cognitive Bias | Lỗi hệ thống trong tư duy | Defaults, anchoring, framing |
| 15 | Mental Model | User kỳ vọng app hoạt động như họ nghĩ | Research user's model, then design to match |
| 16 | Zeigarnik Effect | Chưa hoàn thành → nhớ lâu hơn | Progress bars, "continue where you left off" |
| 17 | Hick's Law | Nhiều lựa chọn = chậm hơn | Giảm choices tại decision points |
| 18 | Choice Overload | Quá nhiều options → paralysis | Recommendations, curated defaults |
| 19 | Occam's Razor | Giải pháp đơn giản nhất thường tốt nhất | Remove unnecessary features/elements |
| 20 | Pareto Principle | 80% impact từ 20% features | Focus design effort on most-used features |
| 21 | Tesler's Law | Complexity không mất, chỉ chuyển đi | Absorb complexity vào system, away from user |
| 22 | Goal-Gradient Effect | Càng gần đích càng cố gắng hơn | Progress bars, boosted start |
| 23 | Peak-End Rule | Nhớ đỉnh và cuối, không phải trung bình | Design wow moments + great endings |
| 24 | Paradox of Active User | User không đọc manual | Design self-explanatory, not documentation |
| 25 | Parkinson's Law | Task mở rộng đến hết thời gian | Set deadlines, show estimated time |
| 26 | Fitts's Law | Target lớn + gần = dễ tap | 44px min touch target, CTA ở vùng thumb |
| 27 | Doherty Threshold | <400ms = productive interaction | Performance = UX; skeleton screens |
| 28 | Postel's Law | Accept flexible, output strict | Fuzzy input, consistent output |
| 29 | Flow | Vừa sức + không gián đoạn = engaged | Remove interruptions, progressive challenge |
| 30 | Jakob's Law | User expect your app = other apps | Follow platform conventions for base patterns |

---

## Cách dùng file này với Gem

Khi research một vấn đề UX, hỏi Gem:
```
Luật UX nào áp dụng cho [VẤN ĐỀ]? Giải thích cơ chế và đưa ra recommendation.
```

Hoặc tra cứu ngược:
```
Tôi muốn [MỤC TIÊU]. Luật nào hỗ trợ điều này và tôi nên thiết kế thế nào?
```

---

*Source: lawsofux.com by Jon Yablonski | License: CC BY-NC-ND 4.0*
*File này tổng hợp và bổ sung phần ứng dụng thực tế. Nội dung gốc thuộc Jon Yablonski.*
