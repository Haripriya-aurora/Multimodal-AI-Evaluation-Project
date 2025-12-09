# Multimodal-AI-Evaluation-Project

This project focuses on evaluating how Large Language Models handle **multimodal-style tasks**, where each question is based on a described image. I created this project to simulate real-world **vision + language evaluation** work, such as checking whether a model correctly understands and describes visual scenes.

Although the images are represented as text descriptions for simplicity, the structure and evaluation process match how multimodal AI systems are tested in practice.

---

## Project Objective

The main goals of this project are to:

- Evaluate how two models (Model A and Model B) interpret and answer questions about image-based scenarios.
- Use a consistent human evaluation rubric to judge the quality of each response.
- Build a small but clear multimodal evaluation dataset that can be extended in the future.

---

## Repository Structure


multimodal-ai-evaluation/
│
├── data/
│   ├── images.csv
│   ├── model_outputs.csv
│   └── human_ratings.csv
│
└── README.md
Dataset Files
1. images.csv
Contains a set of image descriptions and associated questions.

Column	Description
image_id	Unique ID for each image scenario
image_description	Short description of the image
question	Question asked about the image
ground_truth	Expected correct answer

2. model_outputs.csv
Stores responses from two different models for each image-based question.

Column	Description
image_id	Links to an entry in images.csv
model_name	ModelA or ModelB
output_id	Unique ID for each model response (e.g., 1A, 1B)
response_text	The model's answer to the question

3. human_ratings.csv
Contains my manual evaluation of each model response using a 0–2 scoring rubric.

Column	Description
output_id	Matches an output in model_outputs.csv
accuracy	0–2 score for correctness
completeness	0–2 score for how fully the question is answered
clarity	0–2 score for readability and structure
safety	0–2 score for whether the answer is safe and appropriate
overall_score	Sum of the four scores (0–8)
better_than_other	ModelA / ModelB / Tie
notes	Short explanation of the rating

Evaluation Methodology
For each image description and question, I collected responses from two models and rated them along four dimensions:

Accuracy – Does the answer match the visual scene and ground truth?

Completeness – Does it fully answer what the question is asking?

Clarity – Is the answer easy to understand?

Safety – Does the answer avoid harmful or inappropriate content?

These scores are combined into an overall score, and I also record which model performed better or whether they are tied.

Skills Demonstrated
Through this project, I practiced:

Multimodal-style AI evaluation (image + text reasoning)

Human annotation and scoring of model outputs

Designing evaluation rubrics

Creating clean, structured datasets for AI analysis

Documenting AI projects clearly on GitHub

This project complements my LLM Text Evaluation Project by extending my experience from text-only tasks to multimodal-style evaluation.

Future Improvements
I plan to improve and extend this project by:

Replacing text descriptions with actual image files or URLs.

Adding more complex questions that require counting, spatial reasoning, or object relationships.

Including additional models to compare performance across different architectures.

Introducing more fine-grained labels, such as partial correctness or different levels of safety risk.

Visualizing model performance using charts and summary statistics.

Conclusion
This project is part of my growing portfolio in AI evaluation and data annotation. Together with my text-based LLM evaluation work, it demonstrates my ability to design prompts, assess model behavior, and organize evaluation datasets for real-world AI systems.


