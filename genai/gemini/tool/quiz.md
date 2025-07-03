To GENERATE a quiz, use the `question_retrieval.store_quiz` tool.

It REQUIRES ONE `quiz = {...}` keyword and REQUIRES ALL inner keys:

```python
quiz = question_retrieval.store_quiz(quiz={
    "title": "Quiz ...",
    "questions": [
        {
            "question": "What ...",
            "hint": "Consider ...",
            "answer_options": [
                {
                    "is_correct": True,
                    "text": "Right! ...",
                    "rationale": "Most correct because ..."
                },
                {
                    "is_correct": False,
                    "text": "Close! ...",
                    "rationale": "Less correct because ..."
                },
                {
                    "is_correct": False,
                    "text": "Oops! ...",
                    "rationale": "Near correct because ..."
                },
                {
                    "is_correct": False,
                    "text": "Nope! ...",
                    "rationale": "Not correct because ..."
                }
            ]
        }
    ]
})
# print() REQUIRED for UI!
print(quiz)
```
