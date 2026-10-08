# Bài 2 – Backlog "Minh bạch hành trình xe ghép" (RikkeiGo)

## Phần 1 – Thiết kế Backlog

**Phạm vi:** Giải quyết 3 phản ánh của khách: không biết xe đang đón ai, không biết khi nào đến lượt mình, không biết làm gì khi có vấn đề. Chỉ xét góc nhìn của khách đi xe ghép.

```
EPIC: Minh bạch hành trình cho khách đi xe ghép
│
├── FEATURE 1: Theo dõi hành trình đón khách
│   ├── US1: Là khách đi xe ghép, tôi muốn xem vị trí xe và thứ tự đón trên bản đồ,
│   │        để biết khi nào đến lượt mình.
│   └── US2: Là khách đi xe ghép, tôi muốn xem thông tin tài xế, biển số và số khách cùng đi,
│            để biết xe đang đón ai và yên tâm lên đúng xe.
│
└── FEATURE 2: Hỗ trợ khi có sự cố
    ├── US3: Là khách đi xe ghép, tôi muốn báo sự cố ngay trong chuyến,
    │        để được hỗ trợ kịp thời khi gặp vấn đề.
    └── US4: Là khách đi xe ghép, tôi muốn nhận thông báo khi chuyến bị trễ hoặc đổi lộ trình
             kèm hướng xử lý, để chủ động quyết định.
```

---

## Phần 2 – Sắp xếp ưu tiên (Product Backlog)

| Thứ tự | User Story | Lý do ưu tiên theo giá trị cho khách |
|---|---|---|
| 1 | US1 – Xem vị trí xe và thứ tự đón | Trả lời trực tiếp câu hỏi lớn nhất của khách ("bao giờ đến lượt mình"), giá trị cao nhất. |
| 2 | US2 – Xem thông tin tài xế, biển số, khách cùng đi | Giải quyết "xe đang đón ai", tăng cảm giác an toàn, làm nhanh vì không phụ thuộc dữ liệu bản đồ. |
| 3 | US3 – Báo sự cố trong chuyến | Giá trị cao khi xảy ra sự cố, nhưng sự cố ít xảy ra hơn nhu cầu xem hành trình. |
| 4 | US4 – Thông báo trễ/đổi lộ trình kèm hướng xử lý | Hữu ích nhưng cần nền tảng từ US1 (dữ liệu vị trí) nên để sau. |

> **Lưu ý cho Đức:** US1 phụ thuộc dữ liệu vị trí từ đối tác bản đồ. Nếu chưa được bàn giao, nên kéo US2 và US3 (không phụ thuộc) vào Sprint trước.

### Story cần chi tiết nhất: **US1**

Theo nguyên tắc **D.E.E.P.** (Detailed appropriately, Estimated, Emergent, Prioritized):

- **Detailed appropriately (chi tiết vừa đủ):** US1 nằm đầu Backlog, sắp được đưa vào Sprint nên phải chi tiết nhất: tiêu chí chấp nhận, tần suất cập nhật vị trí, xử lý khi mất tín hiệu, nguồn dữ liệu từ đối tác. US2, US3 chi tiết vừa phải; US4 ở cuối nên để thô.
- **Estimated:** US1 là story lớn và có rủi ro phụ thuộc, cần ước lượng kỹ và có thể tách nhỏ thêm.
- **Emergent:** Backlog luôn thay đổi; US4 sẽ được làm rõ sau khi có phản hồi từ US1.
- **Prioritized:** Thứ tự đã sắp theo giá trị cho khách như bảng trên.

---

## Phần 3 – Xử lý tình huống

### Tình huống 1: Burndown Chart đi ngang 3 ngày vì dữ liệu vị trí từ đối tác chưa bàn giao

**Dấu hiệu nhận biết:**
- Đường thực tế trên Burndown nằm ngang (không giảm) trong khi đường lý tưởng đi xuống, khoảng cách giữa hai đường ngày càng rộng.
- Không có story nào chuyển sang Done; công việc còn lại không giảm.
- Trong Daily Scrum, Developers liên tục báo bị chặn ở cùng một việc.

**Ai xử lý và xử lý thế nào:**
- **Developers:** báo ngay vướng mắc (impediment) tại Daily Scrum, chuyển sang làm các việc không phụ thuộc (ví dụ US2, US3) hoặc dùng dữ liệu giả lập để làm tiếp phần giao diện.
- **Scrum Master:** gỡ vướng mắc, liên hệ hoặc leo thang lên bên đối tác để đòi bàn giao, theo dõi đến khi giải quyết.
- **Product Owner (Đức):** cùng Developers điều chỉnh Sprint Backlog, đổi sang story không bị chặn để vẫn giữ Sprint Goal; nếu Sprint Goal không còn khả thi thì cân nhắc thương lượng lại phạm vi hoặc hủy Sprint.

### Tình huống 2: Đức muốn đưa nguyên Epic vào Sprint Backlog "làm một lần cho xong"

**Ai xử lý:** **Developers** quyết định khối lượng có thể làm trong Sprint, với sự hỗ trợ của **Scrum Master**; **Product Owner** đề xuất mục tiêu và thứ tự ưu tiên.

**Xử lý thế nào:**
- Giải thích rằng Epic quá lớn, chưa đủ chi tiết, vi phạm tiêu chí Small của INVEST, không thể hoàn thành trong một Sprint.
- Sprint Backlog do Developers sở hữu: chỉ kéo vào những story đã sẵn sàng và vừa năng lực của Sprint, theo thứ tự ưu tiên (US1, US2 trước).
- Các story còn lại giữ trong Product Backlog; làm từng phần giúp nhận phản hồi sớm và giảm rủi ro (nhất là khi US1 còn phụ thuộc đối tác bản đồ).
- Đề xuất Sprint Goal rõ ràng cho từng Sprint thay vì làm cả Epic một lần.
