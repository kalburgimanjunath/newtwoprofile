---
published: false
layout: post
author: manjunath
categories:
  - projects
image: assets/images/6.jpg
tags: featured
---
## Building MCQ react simple app with sample code

In this article I am going to build a sample application to build react MCQ example.
```
import React from 'react';
import './style.css';
import {
  AddQuestion,
  DisplayQuestion,
  AnswerContainer,
} from './components/index';
import { sampleData } from './data/sampleData';
export default function App() {
  return (
    <>
      <div style={{ width: '100%', display: 'flex', height: '100%' }}>
        <div className="question-container">
          <DisplayQuestion questions={sampleData} />
        </div>
        <AnswerContainer />
      </div>
    </>
  );
}

styles.css

.question-item {
  flex: 1;
  margin-bottom: 20px;
}
.question-container {
  /* display: flex; */
  width: 100%;
  /* flex-direction: row; */
  padding: 20px;
  height: 100%;
}
.answer-container {
  width: 50%;
}
.answer-container textarea {
  padding: 20px;
  width: 100%;
  height: 100%;
}


sampleData.js

export const sampleData = [
  {
    id: 1,
    text: 'Question 1',
    type: 'MCQ',
    answers: ['a', 'b', 'c', 'd'],
    samples: ['a-z', 'b-z'],
    currectAnswer: 'a',
  },
  {
    id: 2,
    text: 'Question 2',
    type: 'MCQ',
    answers: ['a', 'b', 'c', 'd'],
    samples: ['a-z', 'b-z'],
    currectAnswer: 'a',
  },
  {
    id: 3,
    text: 'Question 3',
    type: 'MCQ',
    answers: ['a', 'b', 'c', 'd'],
    samples: ['a-z', 'z-a'],
    currectAnswer: 'a',
  },
  {
    id: 4,
    text: 'Question 4',
    type: 'MCQ',
    answers: ['a', 'b', 'c', 'd'],
    samples: ['a-z', 'z-a'],
    currectAnswer: 'a',
  },
];
AddQuestion.js
import React from 'react';
export default function AddQuestion() {
  return (
    <>
      <h1>Add Question</h1>
      <label>Problem Statement</label>
      <textarea></textarea>
      <label>Expected Answer</label>
      <textarea></textarea>
    </>
  );
}
AnswerContainer.js
import React from 'react';
export default function AnswerContainer() {
  return (
    <div className="answer-container">
      <textarea></textarea>
    </div>
  );
}
DisplayQuestion.js
import React, { useState, useEffect } from 'react';
export default function DisplayQuestion({ questions }) {
  // console.log(questions);
  const [records, setRecord] = useState();
  const [mcqAnswer, setMcqAnswer] = useState();
  useEffect(() => {
    var itemRandom = questions[Math.floor(Math.random() * questions.length)];
    // console.log(itemRandom);
    setRecord(itemRandom);
  }, [questions]);
  function changeValue(e) {
    // console.log(e.target.value);
    setMcqAnswer(e.target.value);
    validateAns(e.target.value, records);
  }
  function validateAns(enteredValue, records) {
    // console.log(enteredValue);
    if (enteredValue == records.currectAnswer) {
      // console.log(enteredValue);
      console.log('correct answer');
    } else {
      console.log('wrong answer');
    }
  }

  const QuestItem = ({ question }) => {
    // console.log(question);
    return (
      <div className="question-item">
        <div>Type:{question.type}</div>
        <div>Question:{question.text}</div>
        <div>
          Answers:
          {question.answers &&
            question.answers.map((item) => {
              // console.log(item);
              return (
                <div key={item.id} style={{ display: 'flex' }}>
                  <input
                    type="radio"
                    name="answer"
                    value={item}
                    onChange={(e) => changeValue(e)}
                  ></input>
                  <label>{item}</label>
                </div>
              );
            })}
        </div>
        <div>Samples Input:{question.samples}</div>
        {mcqAnswer ? <div>Selected Answer:{mcqAnswer}</div> : null}
      </div>
    );
  };
  return (
    <>
      {/* <label>Problem Statement</label> */}
      {records ? <QuestItem question={records} /> : <div>Loading...</div>}
    </>
  );
}
index.js
import AddQuestion from './AddQuestion';
import DisplayQuestion from './DisplayQuestion';
import AnswerContainer from './AnswerContainer';
export { AddQuestion, DisplayQuestion, AnswerContainer };


```
