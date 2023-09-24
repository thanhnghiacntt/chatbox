# Chatbox

## Deploy

**Docker**

Build từ máy local:

```shell
docker build -t chatgpt-ui .
docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 chatgpt-ui
```

Pull từ github:

```
docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 ghcr.io/thanhnghiacntt/chatbox:main
```

## Running Locally

**1. Tải repository về**

```bash
git clone https://github.com/thanhnghiacntt/chatbox.git
```

**2. Cài đặt các Dependencies**

```bash
npm i
```

**3. Cung cấp OpenAI API Key**

Tạo một file ở máy local .env.local để chứa nội dung biến môi trường với OpenAI API key:

```bash
OPENAI_API_KEY=YOUR_KEY
```

**4. Run Ứng dụng**

```bash
npm run dev
```

**5. Truy cập**

Bạn sẽ có thể bắt đầu trò chuyện.

## Cấu hình biến môi trường

Khi chạy ứng dụng bạn có thể sét những biến môi trường sau:

| Tên biến môi trường              | Giá trị mặc đinh                 | Mô tả                                                                                                                               |
| --------------------------------- | ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| OPENAI_API_KEY                    |                                | Cái này là key tạo từ OpenAI, không thể thiếu                                                                                    |
| OPENAI_API_HOST                   | `https://api.openai.com`       | TUrl cơ bản để sử dụng Azure`https://<endpoint>.openai.azure.com`                                                                         |
| OPENAI_API_TYPE                   | `openai`                       | Loại api tùy chọn là `openai` hoặc `azure`                                                                                             |
| OPENAI_API_VERSION                | `2023-03-15-preview`           | Chỉ áp dụng cho Azure OpenAI                                                                                                          |
| AZURE_DEPLOYMENT_ID               |                                | Cần thiết khi Azure OpenAI, Ref[Azure OpenAI API](https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/reference#completions) |
| OPENAI_ORGANIZATION               |                                | Tổ chức OpenAI của bạn                                                                                                               |
| DEFAULT_MODEL                     | `gpt-3.5-turbo`                | Mô hình mặc định để sử dụng cho các cuộc hội thoại mới, dành cho việc sử dụng Azure `gpt-35-turbo`                                                               |
| NEXT_PUBLIC_DEFAULT_SYSTEM_PROMPT | [see here](utils/app/const.ts) | Lời nhắc hệ thống mặc định để sử dụng trên thiết bị mới conversations                                                                                     |
| NEXT_PUBLIC_DEFAULT_TEMPERATURE   | 1                              | Nhiệt độ mặc định để sử dụng trên máy mới conversations                                                                                       |
| GOOGLE_API_KEY                    |                                | Click [Link tài liệu JSON API][GCSE]                                                                                          |
| GOOGLE_CSE_ID                     |                                | Click [Link tài liệu JSON API][GCSE]                                                                                          |

Nếu bạn không có key OpenAI, bạn có thể truy cập vào link đây [here](https://platform.openai.com/account/api-keys).

## Contact

Nếu có bất kỳ câu hỏi nào có thể liên hệ [Facebook](https://www.facebook.com/nguyenthanhnghia.cntt).

[GCSE]: https://developers.google.com/custom-search/v1/overview
