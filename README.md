# WhatsApp Message Sender via URL Parameters

This project demonstrates a simple HTML and JavaScript application that sends a WhatsApp message using URL parameters. The script automatically extracts parameters from the URL, constructs an API call to send the message, and logs the response from the API.

## How It Works

The application uses JavaScript (with jQuery) to:
1. Extract parameters from the URL.
2. Construct a request URL to the WhatsApp API service.
3. Send the request to the API.
4. Handle and log the response from the API.

## Usage

To use this script, you need to embed it within an HTML page. When the page loads, it will automatically send a WhatsApp message using the parameters provided in the URL.

### Required URL Parameters

To send a WhatsApp message, the following parameters should be included in the URL:

1. **`url-api`**: This is the base URL of the WhatsApp API service. It specifies the endpoint where the request to send the message will be sent.
   
   - Example: `https://api.callmebot.com/whatsapp.php`

2. **`phone`**: The recipient's phone number, including the country code. This should be in international format without any special characters (like `+`, `-`, or spaces).
   
   - Example: `20123456789` (for a phone number in Egypt)

3. **`text`**: The message text to send. This should be URL-encoded to ensure special characters and spaces are transmitted correctly.
   
   - Example: `Hello%20World%21` (represents the message "Hello World!")

4. **`apikey`**: The API key required to authenticate with the WhatsApp API service. This key is usually provided when you sign up for the service.
   
   - Example: `7790946`

### Example URL

Here’s an example of how you might structure the URL to include the necessary parameters:

https://yourdomain.com/yourpage.html?url-api=https://api.callmebot.com/whatsapp.php&phone=201018922490&text=Hello%20World!&apikey=your_api_key


When the page is accessed with such a URL, the script will:
1. Extract the parameters.
2. Construct the API call URL.
3. Send the WhatsApp message.

### Parameter Extraction

The script uses a function to parse the URL and extract these parameters into a JavaScript object. This allows the script to dynamically adapt to different URL inputs and send messages based on the provided parameters.

### Message Sending

The script constructs a complete API URL using the extracted parameters and sends a GET request using the `fetch` API. It then logs the response to the console and checks if the response indicates a successful message send based on the specific response format of the API.

### Handling Responses

The script checks if the response includes the word 'success' (case-insensitive) to determine if the message was sent successfully. Adjust this logic based on the specific response format of the API you are using.


