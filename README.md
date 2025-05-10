## 💬 WhatsApp Text Messaging API (Python)  
Send text messages via WhatsApp using Maytapi's API with Python.

## 🚀 Features  
- Send text messages via public URLs  
- Send text using Base64 encoded strings  
- Optional captions for text  
- Lightweight HTTP requests via `requests`  
- Environment variable support with `.env`  

## 📦 Installation  
Install the required packages:

```bash
pip install requests python-dotenv
```
## 🔧 Usage Example
```python
from whatsapp_api import WhatsAppAPI  # Replace with your module filename

api = WhatsAppAPI(
    product_id="YOUR_PRODUCT_ID",
    phone_id="YOUR_PHONE_ID",
    api_token="YOUR_API_TOKEN"
)

# Send text message via URL
response = api.send_text_message(
    to="1234567890",
    text_url="https://example.com/text.jpg",
    caption="Check out this text!"
)
print(response)

# Send text message via Base64
response = api.send_text_from_base64(
    to="1234567890",
    base64_data="data:text/plain;base64,...",
    caption="Base64 text message"
)
print(response)

```
## 🔒 Authentication  
Ensure you have the following credentials:  
- Product ID  
- Phone ID  
- API Token
*These can be securely loaded using a .env file.

## 📝 Methods  
- send_text_message(to, text_url, caption=None): Send text via URL

- send_text_from_base64(to, base64_data, caption=None): Send text using Base64 encoding

## 🔍 Error Handling  
The library provides comprehensive error logging and raises exceptions on HTTP errors.

## 📜 License  
MIT License

## 🤝 Support  
For issues or questions, please open a GitHub issue.
