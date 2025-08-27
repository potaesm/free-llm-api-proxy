## Runtime Arguments

- --proxy; to set a proxy
- --verbose; to get all output (very verbose..)
- --disable-logs; to disable logging to file
- --port; to set a port for the serv to run on

## Features

- free and unlimited!
- openai request and response structure!!!
- detailed logging and verbosity options.
- Integrated proxy support. (if u wna be safe)

## Usage

- **Starting the Server**: The Flask server will run on the configured port (default is `80`). Access it at `http://127.0.0.1`.
- **Logs**: If logging is enabled, logs will be saved to `logs.txt`.
- **Proxy**: If a proxy server is required, specify it at runtime (--proxy).
- Now, you can use the openai module to send and receive requests with the following models:

## Functions

browse_web
generate_document
generate_presentation
generate_image (oolala)
generate_spreadsheet

## KNOWN ISSUES PLEASE READ

It is not rare for it to simply not work, that happens

The script does support sending streaming chunks, but the internal API DOES NOT, so there will be NO actual stream, but apps that depends on streaming will still work.If you do want streaming models, go back to the evalsone branch. I don,t think ill be updating it anymore tho. ill remove this when i can potentially get streaming models.

There might be some issues with the CONVERSATION history. The endpoint works in a progressive messages system, so you can't pass existing messages throught the request, so the only solution i had was to tell it the past messages, and that usually works, but not always. It might start saying some stuff like

```text
I understand you've provided conversation history and a new message, but I should respond as myself based on my actual capabilities and instructions.
```

and when that happens, just try again a few more times, or use another model..
