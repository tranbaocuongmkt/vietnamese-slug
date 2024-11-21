Dưới đây là tài liệu README hoàn chỉnh cho module **Vietnamese Slug**:

---

# Vietnamese Slug

**Vietnamese Slug** là một thư viện tiện ích để tạo *slug* chuẩn SEO từ văn bản tiếng Việt và trích xuất ID từ chuỗi *slug*. Thư viện hỗ trợ loại bỏ dấu tiếng Việt và các ký tự không hợp lệ, giúp cải thiện quá trình xử lý URL và SEO.

## Features

- Chuyển đổi chuỗi tiếng Việt thành slug thân thiện với SEO.
- Hỗ trợ tùy chỉnh ký tự phân cách (`separator`).
- Tách và trích xuất ID hợp lệ từ chuỗi slug.

## Installation

Cài đặt thư viện qua npm:

```bash
npm i vietnamese-slug-nodejs
```

## Usage

### Import thư viện

Sử dụng **ES Module** hoặc **CommonJS**:

#### ES Module
```javascript
import { slug_generation, get_id } from "vietnamese-slug-nodejs";
```

#### CommonJS
```javascript
const { slug_generation, get_id } = require("vietnamese-slug-nodejs");
```

### Example

#### 1. **Tạo slug từ chuỗi**

```javascript
const slug = slug_generation("Tiêu đề bài viết tiếng Việt", "-");
console.log(slug); 
// Output: "tieu-de-bai-viet-tieng-viet"
```

Bạn cũng có thể thay đổi ký tự phân cách:

```javascript
const customSlug = slug_generation("Cà phê ngon!", "_");
console.log(customSlug); 
// Output: "ca_phe_ngon"
```

#### 2. **Trích xuất ID từ slug**

```javascript
const id = get_id("tieu-de-bai-viet-123456789");
console.log(id); 
// Output: "123456789"
```

Nếu slug không chứa ID hợp lệ, hàm sẽ trả về `null`:

```javascript
const invalidId = get_id("tieu-de-bai-viet");
console.log(invalidId); 
// Output: null
```

---

## API Reference

### `slug_generation(str: string, separator: string = "-"): string`

- **Mô tả:** Chuyển đổi một chuỗi thành slug chuẩn SEO.
- **Tham số:**
  - `str` *(string)*: Chuỗi gốc cần chuyển đổi.
  - `separator` *(string)*: Ký tự phân cách trong slug (mặc định là `"-"`).
- **Trả về:** Chuỗi slug đã chuẩn hóa.

#### **Ví dụ:**
```javascript
slug_generation("Chào mừng đến với Việt Nam!", "-");
// Output: "chao-mung-den-voi-viet-nam"
```

---

### `get_id(slug: string): string | null`

- **Mô tả:** Trích xuất ID hợp lệ từ cuối slug.
- **Tham số:**
  - `slug` *(string)*: Chuỗi slug chứa ID (dạng `"ten-bai-viet-123456"`).
- **Trả về:** ID *(string)* nếu hợp lệ, hoặc `null` nếu không tìm thấy.

#### **Ví dụ:**
```javascript
get_id("tieu-de-12345");
// Output: "12345"
```

---

## Contributing

Nếu bạn muốn đóng góp cho dự án, vui lòng tạo **Pull Request** hoặc **Issue** tại kho lưu trữ GitHub:  
[GitHub Repository](https://github.com/tranbaocuongmkt/vietnamese-slug)

---

## License

**Vietnamese Slug** được phát hành theo giấy phép [MIT License](LICENSE).

---

## Author

- **Trần Bảo Cường**  
- [GitHub](https://github.com/tranbaocuongmkt)  
- [npm Profile](https://www.npmjs.com/~tranbaocuongmkt)

---

Bạn có thể sử dụng tài liệu này để hướng dẫn người dùng một cách đầy đủ và chi tiết! 🎉