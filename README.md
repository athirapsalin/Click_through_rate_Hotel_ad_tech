# Case Study: Predicting Click-Through Rate (CTR) to Improve Ranking

## Objective:

- This case study aims to evaluate your analytical, modeling, and presentation skills. The goal is to predict the likelihood of an accommodation being clicked by a user (Click-Through Rate, CTR).
- This case represents a simplified version of challenges you may encounter in the role at trivago. Please keep the case confidential. The datasets are anonymized and randomized specifically for this case study.
- **Submission Deadline:** 7 days from receiving the case study.
- Upon review, you will be invited to a technical interview to discuss your approach, findings, and other technical skills.

## Glossary:

- **Click-Through Rate (CTR):** The probability that a user will click on a specific accommodation when it appears in search results.
- **Ranking Algorithm:** A system that orders search results based on various criteria, including predicted CTR, to optimize user engagement.

## Datasets Overview:

Whenever a search for  a specific accommodation or city is triggered on our website, the ranking algorithm orders accommodations based on certain criteria and presents them to the user. This data, along with the user's feedback (whether an item is clicked or not), is logged for a short period in `train-data.csv`. Additionally, you can find item metadata in the `item.csv` file. You can find more details about each file below:

### **train.csv, test.csv**

Contains user search data, including whether an item was clicked (`is_clicked_item`). This data helps learn about user behavior and improve the ranking algorithm. Key columns include:
- `ymd`: train-csv.csv is This the day 
- `user_id`: Unique identifier for the user
- `search_id`: Unique identifier for the search event
- `item_id`: Unique identifier for the accommodation
- `platform`: Platform/country used by the user (e.g., c1, c2, c3 can be .fr, .de, .com)
- `device`: Device used for the search
- `search_type`: Type of search (0 for city search, 1 for accommodation search)
- `item_position`: Position of the accommodation in the displayed result list 
- `price`: Price of the  accommodation
- `is_clicked_item`: Indicator of whether the accommodation was clicked

**Note:** The `test.csv` file has the same structure without the ground truth (`is_clicked_item`).

### **item.csv**

Contains additional attributes for accommodations, including item ID, city ID, accommodation type, stars, ratings, and number of ratings. Key columns include:
- `item_id`: Unique identifier for the accommodations
- `city_id`: Identifier for the city where the accommodations is located
- `accommodation_type_id`: Type of accommodation (hotel, hostel, apartment)
- `star`: Number of stars for the accommodations
- `avg_rating`: Average user rating for the accommodations (0 to 10 scale)
- `num_rating`: Number of ratings received

## Tasks:

### Task 1: CTR Prediction Model

Develop a model to accurately predict whether a user will click on an accommodation/item (`is_clicked_item`) using the training dataset.
- **Develop a model to predict CTR (i.e.value for `is_clicked_item`).**
    - What are the potential solutions to predict the click-through rate?
    - Please pick your best solution and write Python code that generates the prediction result for the test dataset.

- **Evaluate the model**
    - How will you evaluate the model?
    - Please pick one or a few metrics that you think are worth presenting and write Python code to generate the evaluation results.

- **Predict the CTR for the test dataset:**
    - Provide predictions for  is_clicked_item in the test dataset (`test-data.csv`), focusing on the probability of clicks for each item (i.e., `prob(is_clicked_item=1)`). Submit the results with columns for `user_id`, `search_id`, `item_id`, and `prob`.

### Task 2: Create Your Presentation

Summarize your key findings from the model development process. Specifically, we are interested in:
- Key findings during the model development.
- Your approach to model selection, including critical challenges and decision points.
- How you believe your model performs in terms of ranking.

## Deliverables:

- **Code and Analysis:** A Jupyter Notebook containing the answers to Task 1.
- **Test Results:** A CSV file with prediction results for each `user_id`, `search_id`, and `item_id` combination available in `test-data.csv`.
- **Presentation File:** A document summarizing your key findings and specific features of your model.
 
### How to use the code input 
- open jupyter notebook
- install Requirements using pip install -r Requirements.txt
- save train.csv , tes.csv and item.csv in the same folder as the code
- Run entire code it may 130 minutes 
- prediction_results.csv will be added or replace the 'path' in the df_test_predcitiionto_csv('path')

## Authors

- ATHIRA PULICKKAUDY SALIN

