# Portkey Gateway: Your Gateway to Multiple AI APIs

Portkey gateway is a user-friendly tool acting as a bridge between the OpenAI API and numerous other AI APIs, including Google AI, Cohere,
and more. This allows you to access and utilize different AI models from various providers through a single, unified interface.

**Key Features:**

* **Multi-Provider Support:** Access models from Google AI, Cohere, and others through the familiar OpenAI API interface.
* **Easy Configuration:** Simple setup using environment variables or a configuration file.
* **Streamlined Workflow:** No need to learn different APIs or manage multiple API keys.
* **Flexibility:** Choose the best model for your specific needs and budget from a variety of providers.

**Getting Started:**

1. **Install Portkey Gateway:** Follow the instructions on the [Portkey GitHub repository](https://github.com/Portkey-AI/gateway). Easiest to simply run it under Docker.
2. **Configure your API Keys:** Set your API keys for the desired providers as environment variables or in the configuration file(s).
3. **Choose your Model:** Select the desired model using the `x-portkey-provider` header and the model name.
4. **Start using the OpenAI API:** Make requests to the OpenAI API endpoint as usual, and Portkey will route them to the appropriate provider.

**Example Configuration:**

To use Google AI's `gemini-1.5-pro-latest` model, you would set the following environment variables, or edit the config file to be like this:

```
EXTRA_HEADERS=x-portkey-provider,google
API_BASE_URL=http://localhost:8787/v1
OPENAI_API_KEY=YOUR_GOOGLE_API_KEY
DEFAULT_MODEL=gemini-1.5-pro-latest                                                                                                   ```

For Anthropic, max_tokens is required.

```
EXTRA_HEADERS=x-portkey-provider,anthropic
API_BASE_URL=http://localhost:8787/v1
OPENAI_API_KEY=ANTHROPIC_KEY
DEFAULT_MODEL=claude-3-opus-20240229
MAX_TOKENS=4000
```

Another tip is to add your various config files and symlink them to .sgpt so that it's reasonably easy to switch.

```
EXTRA_HEADERS=x-portkey-provider,groq
API_BASE_URL=http://localhost:8787/v1
OPENAI_API_KEY=gsk_GROQ_API_KEY
DEFAULT_MODEL=mixtral-8x7b-32768
```

OpenAI is also supported via the proxy.

```
EXTRA_HEADERS=x-portkey-provider,openai
API_BASE_URL=http://localhost:8787/v1
OPENAI_API_KEY=sk-OPENAI_KEY
DEFAULT_MODEL=gpt-3.5-turbo
```
