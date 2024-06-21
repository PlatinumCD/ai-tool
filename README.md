# AI Thread Management

This project facilitates efficient management and communication with an AI assistant through handling threads and structured messages. It allows users to interact with the OpenAI assistant, send formatted messages, and retrieve generated responses, saving them as files in a well-structured directory format.

## Table of Contents

1. [Features](#features)
2. [Usage](#usage)
3. [Directory Structure](#directory-structure)

## Features

- **Automated API Key Handling:** Reads the OpenAI API key from a specified file.
- **Thread Management:** Automatically creates or retrieves threads for structured conversations.
- **Message Formatting:** Supports inclusion of focus files, context files, and multiple external files in messages.
- **File Handling:** Gathers files from specified directories (both flat and recursive) and generates organized file outputs.
- **CLI Integration:** Provides a command-line interface for easy script execution with various options.

## Usage

The project can be executed via the command-line interface. Here are some examples:

1. **Basic Usage:**
   Send a message to the assistant with a focus file and context:
   ```shell
   python ai -m "Summarize the project's purpose" -ff path/to/focusfile -c path/to/contextfile
   ```

2. **Include External Files:**
   Include multiple specific files:
   ```shell
   python ai -m "Please review these files" -x path/to/external1 -x path/to/external2
   ```

3. **Include Files from Directories:**
   Include all matching files from specified directories:
   ```shell
   python ai -m "Analyze these directories" -xd dir1 -xd dir2
   ```
   Or recursively include from directories:
   ```shell
   python ai -m "Analyze these directories recursively" -xr dir1 -xr dir2
   ```

## Directory Structure

The project creates and manages several directories:

- `AI_THREAD/`: Base directory for storing thread information.
  - `thread`: A file storing the current thread's metadata.
  - `GEN_FILES_<num>/`: Subdirectories holding generated files from AI responses.
