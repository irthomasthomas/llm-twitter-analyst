# llm-twitter

[![PyPI](https://img.shields.io/pypi/v/llm-twitter.svg)](https://pypi.org/project/llm-twitter/)
[![Changelog](https://img.shields.io/github/v/release/yourusername/llm-twitter?include_prereleases&label=changelog)](https://github.com/yourusername/llm-twitter/releases)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/yourusername/llm-twitter/blob/main/LICENSE)

LLM plugin for answering questions about Twitter profiles. 

### Inspired by a [BM](https://github.com/bm-github) project.

## Installation

Install this plugin in the same environment as [LLM](https://llm.datasette.io/):

```bash
llm install llm-twitter
```

## Configuration

Set your Twitter API bearer token as an environment variable:

```bash
export TWITTER_BEARER_TOKEN="your_twitter_bearer_token_here"
```

You can obtain a bearer token by applying for a Twitter Developer account and creating an application at https://developer.twitter.com/

## Usage

To use the llm-twitter plugin, run the following command:

```bash
llm twitter "Your question about the Twitter profile" --account @username
```

Options:

- `--account` or `-a`: Twitter account (username or @username) - required
- `--no-stream`: Do not stream output
- `--force-refresh` or `-f`: Force refresh of the cached profile
- `--model` or `-m`: Specify a different LLM model to use for the response

Examples:

```bash
llm twitter "What is the user's follower count?" --account @openai
llm twitter "Summarize the user's bio" --account @elonmusk --no-stream
llm twitter "What are the main topics this user tweets about?" --account @ylecun --force-refresh
llm twitter "Analyze the user's Twitter presence" --account @google --model gpt-4
```

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:

```bash
cd llm-twitter
python -m venv venv
source venv/bin/activate
```

Now install the dependencies and test dependencies:

```bash
pip install -e '.[test]'
```

To run the tests:

```bash
pytest
```

## Contributing

Contributions to llm-twitter are welcome! Please refer to the [GitHub repository](https://github.com/yourusername/llm-twitter) for more information on how to contribute.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.
