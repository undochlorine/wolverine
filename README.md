# Wolverine

## About

Give your scripts regenerative healing abilities!

Run your scripts with Wolverine and when they crash, GPT-4 edits them and explains what went wrong. Even if you have many bugs it will repeatedly rerun until it's fixed.

Add your openAI api key to `.env`

#### The Wolverine supports .go files to be executed now!  
## Setup step by step:

    1) git clone  https://....<the_link>
    2) cd internal/main
    3) go mod install
    4) go build -o ../../your_wish_folder/wolverine.exe
    5) cd ../../your_wish_folder
    6) > .env
    7) fill the .env file like in the example below, but with your personal data

### Example .env:
    OPENAI_API_KEY=gorinfwe:mfwbevnmowemo9fn20f439vn03v4
    GPT_MODEL=text-davinci-003
    ATTEMPTS_TO_TRY=15

#### Remember that each attempt is a request to GPT so think twice about \<ATTEMPTS_TO_TRY> value
#### GPT 4 is the most preferable model here, but you can try to use any model

## Example Usage

    ./wolverine.exe main

#### main here is your filename WITHOUT .go extension
#### If you see the "Success" message, then you must have obtained a file enterFilename+"__fixed".go>, and it's free of any compile errors. So you can freely run it
    go run main__fixed.go
