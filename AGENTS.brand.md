<!-- semi-brand:start -->
## Brand: 3dnoobs (`@3dnoobs/brand`)

This product belongs to the **3dnoobs** brand. Colours, fonts, logo, voice and allowed styles come only from `@3dnoobs/brand` (full guideline: `node_modules/@3dnoobs/brand/BRAND.md`; with the Semi MCP server, `semi_brand` answers from it).

**Colour**
- Accent use: **Cân bằng**. Như tiết chế, thêm nền nhạt bg-accent-subtle cho khối nổi bật (banner, thẻ khuyến nghị), tối đa một khối mỗi màn hình.
- Share of a screen, roughly: neutral 70%, surface 20%, accent 10%.
- One primary button per area (`Button variant="primary"`); everything else secondary or ghost.
- States: `ring-focus`, `border-focus`, `bg-accent-subtle`, `border-accent-line`; coloured text `text-accent-fg`. Never `primary-500/15`-style classes (`accent-state-token`).
- This brand has no secondary colour: do not add one.
- Status (success, error, warning) keeps Semi's status tokens, never the brand colour.
- Never define brand colours or override Semi tokens in this app (`--color-primary-*`, `--semi-*`, `@theme` colours, hex values): `semi-lint` blocks it (`brand-override`).

**Type and style**
- Style: `flat`, `soft` only (`data-style` on `<html>`, `"style"` in `semi-lint.json`, switch on request).
- Fonts: Geist + Montserrat Alternates, loaded with `next/font` in the root layout (`--font-geist`, `--font-montserrat-alternates`). Titles `font-display`, big numbers `font-figure`, everything else `font-sans`.

**Logo**
- Import from `@3dnoobs/brand/dist/logo/full.svg` (dark theme: `@3dnoobs/brand/dist/logo/fullDark.svg`). Never redraw, recolour or stretch it.
- Clear space 0.5 × its height; full logo at least 80px wide.

**Voice (UI text)** — Thân thiện. Address the user as “bạn”; the brand says “3D Noobs”. Emoji: none. Write UI text in the product's language (Vietnamese unless the product says otherwise).
- Nói chuyện trực tiếp với người dùng, câu ngắn, ấm áp
- Được dùng câu cảm ơn ngắn sau một việc lớn (đặt hàng, tạo xong)
- Không đùa trong thông báo lỗi
- Nút: động từ + đối tượng, tối đa 3 từ, viết hoa chữ đầu (Lưu, Tạo đơn hàng), không "OK" / "Xác nhận" chung chung
- Lỗi: chuyện gì xảy ra + cách sửa, không đổ lỗi cho người dùng, không mã lỗi trần
- Trạng thái trống: vì sao trống + một hành động để bắt đầu
- Không viết "Đang tải…": dùng skeleton hoặc thanh tiến trình
- Không phụ đề dưới tiêu đề trang; nhãn ngắn, icon đi trước chữ
- Do: Nói như một người bạn đã in 3D lâu năm: giải thích thuật ngữ bằng lời thường khi người dùng có thể là người mới.
- Do: Khuyến khích thử nghiệm và chỉ rõ bước tiếp theo, kể cả khi có lỗi.
- Don't: Không chê hay làm người dùng thấy mình "noob" khi họ hỏi hoặc làm sai.
- Don't: Không đùa trong thông báo về tiền, đơn hàng hay lỗi làm mất dữ liệu.
- Example (button): “Thêm vào giỏ” · “Bắt đầu in” · “Chia sẻ mẫu”
- Example (error): “Chưa tải được file của bạn. Kiểm tra kết nối rồi thử lại nhé.”
- Example (empty): “Bạn chưa có mẫu nào. Tải lên mẫu đầu tiên hoặc xem thư viện của cộng đồng để lấy cảm hứng.”

**Who it is for** — Mọi người quan tâm đến in 3D, từ người mới bắt đầu dùng điện thoại đến maker và kỹ sư làm việc trên máy tính; personality: thân thiện, vui vẻ, sáng tạo. Choose words and imagery for them.

**Sample content** — placeholders, seed data and empty states use this product's own things: main list “Mẫu in”; items “Móc khoá logo PLA đen”, “Giá đỡ điện thoại PETG”, “Hộp đựng linh kiện in nhiều màu”; main figure “Bản in tháng này” (128). Never "Lorem", "John Doe" or another domain.

**Imagery** — Ảnh chụp thật máy in, vật liệu và mô hình do cộng đồng in; ánh sáng tự nhiên, nền gọn.

**Density and type scale** are this product's own choice (`data-density`, `data-type-scale` on `<html>`, mirrored in `semi-lint.json`), not the brand's. Big numbers: `<KpiCard featured>`.

**Avoid the generic AI look**
- Not every screen is sidebar + title + four equal KPI cards + a table: give each screen one main block (the thing the user came for) and make it bigger than the rest.
- KPI icons stay neutral or are left out; colour on a KPI means something (`tone="good"|"danger"`), never one decorative colour per card.
- No row of three feature cards with an icon, a one-word title and a vague promise (“Fast”, “Secure”, “Dedicated”). Show proof instead: a product shot, a real number, a customer quote.
- No icon in front of every label: icons where they help scanning (navigation, actions, status), not as decoration.
- Sample and empty-state text comes from this brand's product and voice, never generic (“Lorem”, “John Doe”, “Acme”, orders for a product the brand does not sell).
- Vary the rhythm: not every block a card with the same padding; use plain sections, dividers and white space too.

A change to the brand happens in the brand repo (`/semi-brand`), then `/semi-sync` here.
<!-- semi-brand:end -->
