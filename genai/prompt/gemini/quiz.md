# HOWTO: Quiz Creation

## The Problem
Backend quiz tools—e.g. `question_retrieval.store_quiz`—store quizzes on servers but don't display them to users. Users see nothing despite "success" messages.

## The Solution
Embed quizzes directly using `<immersive type="learning">` tags. No tools, no servers—just direct rendering.

## Essential Structure
````html
<immersive id="unique-id" type="learning" title="Quiz Title">
```quiz
{
  "questions": [
    {
      "question": "Question text?",
      "hint": "Optional hint",
      "answerOptions": [
        {
          "text": "Wrong answer",
          "isCorrect": false,
          "rationale": "Why this is wrong"
        },
        {
          "text": "Correct answer",
          "isCorrect": true,
          "rationale": "Why this is correct"
        }
      ]
    }
  ]
}
```
</immersive>
````

## Critical Rules
- **Unique ID**: Never reuse IDs in the same conversation
- **Valid JSON**: No comments, proper quotes, correct brackets
- **Complete block**: Send entire structure in one response
- **1+ right answer**: More than one `isCorrect: true` allowed
- **All rationales**: Explain every answer option

## Working Example
````html
<immersive id="demo-quiz-001" type="learning" title="Quick Test">
```quiz
{
  "questions": [
    {
      "question": "What makes quizzes visible to users?",
      "hint": "Which one is inherently closer to users?",
      "answerOptions": [
        {
          "text": "Backend storage functions",
          "isCorrect": false,
          "rationale": "Backend functions store but don't display quizzes."
        },
        {
          "text": "Direct embedding with immersive tags",
          "isCorrect": true,
          "rationale": "Correct! Direct embedding renders quizzes in the user interface."
        }
      ]
    }
  ]
}
```
</immersive>
````

## Success Criteria
User sees interactive quiz → Success
User sees nothing → Use this guide
