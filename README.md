Language Translator

A simple Python language translation program built with googletrans. It allows the user to enter a source language, a word or sentence, and a target language, then prints the translated text.

Features

Translate words or sentences between supported languages.

Accept either a language code or a language name.

Examples:

en / english

hi / hindi

lo / lao

Displays a helpful message when an unsupported language is entered.

Handles translation errors with an exception message.

Requirements

Python 3

Google Colab or a Python environment

googletrans==4.0.0-rc1

Installation

Install the required package:

pip install googletrans==4.0.0-rc1

Note: This version of googletrans installs an older httpx version. In environments that already use packages requiring newer httpx, dependency conflicts may occur.

How to Run

Run the notebook and enter:

The language to translate from.

The word or sentence to translate.

The language to translate to.

Example:

Enter language to translate FROM: en
Enter word or sentence: Hello
Enter language to translate TO: hi

Translation:
नमस्ते

You can enter either a language code or language name:

en / english
hi / hindi
lo / lao

How It Works

The program loads the supported languages from googletrans, converts language names to their corresponding language codes, and then uses Translator().translate() to perform the translation.

The main translation logic is:

translation = translator.translate(
    word,
    src=translating_from,
    dest=translating_to
).text

Error Handling

If the entered language is not supported, the program displays:

Unknown language
You can use language code OR language name

Unexpected translation errors are also caught and displayed to the user.

Project Structure

MSME/
├── lang_tran.ipynb
└── README.md

Google Colab

The notebook is configured with a Google Colab link and can be opened directly from the repository.

Repository notebook:

https://github.com/harshkori1/MSME/blob/main/lang_tran.ipynb

License

This project does not currently specify a license.
