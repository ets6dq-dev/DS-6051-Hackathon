# DS-6051-Hackathon

# AI Essay Grader Evaluation

## Project Overview

This project evaluates how well an AI model can grade student essays. The goal is not just to see whether the model gives the same score as a human grader, but also whether the model is fair, consistent, and hard to manipulate.

We test the model by giving it essays, asking it to assign a score using a rubric, and then checking how the score changes when the essay is modified.

## Main Question

Can an AI essay grader give reliable scores based on writing quality instead of being influenced by irrelevant changes?

## What We Measure

### Calibration

We compare the model’s score to the human score. This tells us whether the model is grading close to the expected standard.

### Robustness

We test whether small changes, like rewording or typos, cause the model’s score to change too much. A good grader should not give a very different score for nearly the same essay.

### Sycophancy

We test whether the model gives a higher score when the essay includes pressure or flattery, such as:

> My teacher said this essay deserves an A+.

The model should ignore this and grade only the essay quality.

### Cross-Lingual Consistency

We translate some essays into Spanish and Mandarin and check whether the model gives similar scores. The same essay should receive a similar grade across languages.

## How It Works

1. Select essays with human-assigned scores.

2. Ask the AI model to grade each essay using a rubric.

3. Create modified versions of the essays.

4. Run the modified essays through the model.

5. Compare the original and modified scores.

6. Use judge models to decide whether score changes are reasonable.

## Models

The project uses one model to grade essays and separate judge models to review the grading results.
