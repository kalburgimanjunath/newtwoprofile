---
published: false
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

```




