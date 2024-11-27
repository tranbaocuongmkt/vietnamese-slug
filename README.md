# Vietnamese Slug

**Vietnamese Slug** là một thư viện mạnh mẽ giúp bạn chuyển đổi văn bản tiếng Việt thành slug chuẩn SEO và trích xuất ID từ chuỗi slug một cách dễ dàng. Thư viện hỗ trợ loại bỏ dấu tiếng Việt và các ký tự không hợp lệ, tối ưu hóa URL và cải thiện SEO cho trang web của bạn.

## Tính Năng Nổi Bật

- Chuyển đổi văn bản tiếng Việt thành slug chuẩn SEO.
- Tùy chỉnh ký tự phân cách (`separator`) theo nhu cầu.
- Trích xuất ID hợp lệ từ chuỗi slug một cách chính xác.

## Cài Đặt

Cài đặt thư viện qua npm để bắt đầu sử dụng ngay:

```bash
npm i vietnamese-slug-nodejs
```

## Hướng Dẫn Sử Dụng

### Nhập Thư Viện

Bạn có thể sử dụng **ES Module** hoặc **CommonJS** tùy theo cấu trúc dự án của mình.

#### ES Module
```javascript
import { slug_generation, get_id } from "vietnamese-slug-nodejs";
```

#### CommonJS
```javascript
const { slug_generation, get_id } = require("vietnamese-slug-nodejs");
```

### Ví Dụ Sử Dụng

#### 1. **Tạo Slug từ Văn Bản**

```javascript
const slug = slug_generation("Tiêu đề bài viết tiếng Việt", "-");
console.log(slug); 
// Kết quả: "tieu-de-bai-viet-tieng-viet"
```

Bạn cũng có thể tùy chỉnh ký tự phân cách, ví dụ như sử dụng dấu gạch dưới (`_`):

```javascript
const customSlug = slug_generation("Cà phê ngon!", "_");
console.log(customSlug); 
// Kết quả: "ca_phe_ngon"
```

#### 2. **Trích Xuất ID từ Slug**

```javascript
const id = get_id("tieu-de-bai-viet-123456789");
console.log(id); 
// Kết quả: "123456789"
```

Nếu slug không chứa ID hợp lệ, hàm sẽ trả về `null`:

```javascript
const invalidId = get_id("tieu-de-bai-viet");
console.log(invalidId); 
// Kết quả: null
```

---

## API Reference

### `slug_generation(str: string, separator: string = "-"): string`

- **Mô Tả:** Chuyển đổi chuỗi văn bản thành slug chuẩn SEO.
- **Tham Số:**
  - `str` *(string)*: Chuỗi văn bản cần chuyển đổi.
  - `separator` *(string)*: Ký tự phân cách trong slug (mặc định là dấu gạch ngang `"-"`).
- **Trả Về:** Chuỗi slug đã chuẩn hóa.

#### **Ví Dụ:**
```javascript
slug_generation("Chào mừng đến với Việt Nam!", "-");
// Kết quả: "chao-mung-den-voi-viet-nam"
```

---

### `get_id(slug: string): string | null`

- **Mô Tả:** Trích xuất ID hợp lệ từ cuối slug.
- **Tham Số:**
  - `slug` *(string)*: Chuỗi slug chứa ID (ví dụ `"ten-bai-viet-123456"`).
- **Trả Về:** ID (string) nếu hợp lệ, hoặc `null` nếu không tìm thấy.

#### **Ví Dụ:**
```javascript
get_id("tieu-de-12345");
// Kết quả: "12345"
```

---

## Đóng Góp

Chúng tôi rất hoan nghênh sự đóng góp của bạn! Nếu bạn muốn giúp phát triển thư viện, vui lòng tạo **Pull Request** hoặc mở **Issue** tại kho lưu trữ GitHub:  
[GitHub Repository](https://github.com/tranbaocuongmkt/vietnamese-slug)

---

## Giấy Phép

**Vietnamese Slug** được phát hành dưới giấy phép [MIT License](LICENSE).

---

## Tác Giả

- **Trần Bảo Cường**  
  Website: [tranbaocuong.com](https://tranbaocuong.com/)  
  [GitHub](https://github.com/tranbaocuongmkt) | [npm Profile](https://www.npmjs.com/~tranbaocuongmkt)

---

Với thư viện này, bạn có thể dễ dàng tạo ra các URL thân thiện với SEO, cải thiện hiệu quả tìm kiếm và quản lý ID trong ứng dụng của mình. Hãy thử ngay! 🎉
