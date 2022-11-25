# Neural Grammar Correction
Neural Grammar Correction service for SingularityNET
## Welcome
## What’s the point?
The service receives the source text, and then gives the grammatically correct text
## Model details:
Base model is T5.
The model tries to correct potentially grammatically incorrect text, which may contain many errors, and semantically does not change the text/information that is grammatically correct.
### The user must provide the following inputs in order to start the service and get a response:
#### Inputs:
`text`: json string

Example of input file content:

`[{"text": "the source text 1"}, {"text": "the source text 2"}, ..., {"text": "the source text n"}]`

#### Outputs:
`result`: json string

Example of output file content:

`[{"generated_text": "the correct text 1"}, {"generated_text": "the correct text 2"}, ..., {"generated_text": "the correct text n"}]`

## What to expect from this service?
Inputs:

`[{"text": "There's always a high price to pay for righting wrongs."}, {"text": "It took her two wiks to write her last letter with revisions and corected spelling."}]`

Outputs:

`[{'generated_text': "I've always paid a high price for righting wrongs."}, {'generated_text': 'I took her two weeks to write her last letter with corrections and corrected spelling.'}]`
