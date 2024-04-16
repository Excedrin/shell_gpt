 # Portkey Gateway: Your Gateway to Multiple AI APIs

 Portkey gateway is a user-friendly tool acting as a bridge between the OpenAI API and numerous other AI APIs, including Google AI, Cohere,
 and more. This allows you to access and utilize different AI models from various providers through a single, unified interface.

 **Key Features:**

 * **Multi-Provider Support:** Access models from Google AI, Cohere, and others through the familiar OpenAI API interface.
 * **Easy Configuration:** Simple setup using environment variables or a configuration file.
 * **Streamlined Workflow:** No need to learn different APIs or manage multiple API keys.
 * **Flexibility:** Choose the best model for your specific needs and budget from a variety of providers.

 **Getting Started:**

 1. **Install Portkey Gateway:** Follow the instructions on the [Portkey GitHub repository](https://github.com/Portkey-AI/gateway).
 2. **Configure your API Keys:** Set your API keys for the desired providers as environment variables or in the configuration file.
 3. **Choose your Model:** Select the desired model using the `x-portkey-provider` header and the model name.
 4. **Start using the OpenAI API:** Make requests to the OpenAI API endpoint as usual, and Portkey will route them to the appropriate
 provider.

 **Example Configuration:**

 To use Google AI's `gemini-1.5-pro-latest` model, you would set the following environment variables:
```
EXTRA_HEADERS=x-portkey-provider,google
API_BASE_URL=http://localhost:8787/v1
OPENAI_API_KEY=YOUR_GOOGLE_API_KEY
DEFAULT_MODEL=gemini-1.5-pro-latest                                                                                                   ```
