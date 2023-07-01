
## Add questions

To insert a question add an intent. An intent in context of a chatbot refers to the goal the customer has in mind when typing in a question or comment. While entity refers to the modifier the customer uses to describe their issue, intent is what they really mean. To add intent in faq.yml, just make an entry with the following syntax:

```
  - intent:faq/{name_for_the_question}:
    examples: |
      - {Example phrase1 for question}
      - {Example phrase2 for question}
      - {Example phrase3 for question}
```
- `{name_for_the_question}`:  provide a unique name for the question. For example `ask_smd_bhaio`. NOTE: the question must start with prefix `ask` and should be separated by `_`.
- '{Example phrase for question}` This should contain the question. NOTE: Its RECOMMENDED to provide at least 3 examples for a question with slightly different phrasing.



- An example intent is as follows:

```
- intent: faq/ask_akonnect_privacy
    examples: |
      - Can I trust that my personal information will remain confidential and not be shared with any external parties?
      - Is it possible that my personal data may be shared with third-party organizations without my knowledge or consent?
      - Are there any instances in which my personal details could be sold or given to third parties, and if so, what are they?
      
```



## Add answers

- Follow the syntax below.
```
    utter_faq/{name_for_the_question}:
      - text: "{Answer1 for the question}"
      - text: "{Answer2 for the question}"
      - text: "{Answer3 for the question}"
```
- NOTE: As same as question, it's RECOMMENDED to add multiple examples of answers with different phrasing.
- An example answer is as below:

```
utter_faq/ask_akonnect_privacy:
    - text: "No. Your personal details will only be used to send you messages. You can read the Privacy Policy here. (https://www.dadabhagwan.org/privacy-policy/)"
    - text: "We will only use your personal information to send you messages and will not share it with anyone else. You can review our privacy policy by clicking here (https://www.dadabhagwan.org/privacy-policy/)."
    - text: "Your personal details will be solely used for message delivery purposes and we won't disclose them to any third parties. For more information, please refer to our privacy policy at (https://www.dadabhagwan.org/privacy-policy/)."
  
```



For reference lookup these two files in the source code:

* [data/faq.yml](https://github.com/dadabhagwan/AkramBot/blob/faq/data/faq.yml)
* [domain.yml](https://github.com/dadabhagwan/AkramBot/blob/faq/domain.yml)


