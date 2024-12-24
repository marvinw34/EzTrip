<div align=justify>
  <img src="https://img.shields.io/badge/EzTrip-3DDC84?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white"/>
</div>

<div align=center>
  <h1>EzTrip: AI Travel Companion App in Your Hand!</h1>
  <img src="https://github.com/user-attachments/assets/e5b0cbc4-ed88-47a1-8dc7-b686dc65533b"/>
</div>
<br>
<div align=center>
    <img src="https://img.shields.io/badge/Python-3670A0?&logo=python&logoColor=ffdd54"/>
    <img src="https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?&logo=TensorFlow&logoColor=white"/>
    <img src="https://img.shields.io/badge/Keras-%23D00000.svg?&logo=Keras&logoColor=white"/>
    <img src="https://img.shields.io/badge/Pandas-%23150458.svg?&logo=pandas&logoColor=white"/>
    <img src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?&logo=Matplotlib&logoColor=black"/>
    <img src="https://img.shields.io/badge/Numpy-%23013243.svg?&logo=numpy&logoColor=white"/>
    <img src="https://img.shields.io/badge/Scikit--learn-%23F7931E.svg?&logo=scikit-learn&logoColor=white"/>
    <h3>Machine Learning Models Documentation</h3>
</div>

---

#### Project Overview

EzTrip is an AI-powered travel application designed to offer a more organized, efficient, and sustainable tourism experience. The primary goal of the project is to assist travelers in planning their trips to destinations they are not familiar with. Key features include:

- **Tourist Attraction Recommendations**: Suggestions based on user preferences for accommodation, attractions, and culinary.
- **Expense Tracker**: A feature to monitor the travel budget.
- **Integrated Automatic Generate Itineraries**: Create a generated itineraries based on budget input and city that person wants to visits.
- **Sentiment Analysis**: Using user reviews to provide more relevant recommendations.

##### Project Focus
The initial prototype focuses on Bali, chosen for its global popularity among tourists, making it an ideal location to test data-driven features. The project also promotes sustainable tourism by providing recommendations that prioritize eco-friendly travel options and support local culture.

---

#### Business Understanding

##### Background and Business Objectives
<p align=justify>
Travel planning often requires careful consideration, especially for travelers looking to visit destinations they are unfamiliar with. Information scattered across various platforms can be overwhelming and time-consuming to sift through, making it difficult for travelers to plan trips that align with their preferences. In addition, the tourism industry faces challenges in developing destinations that are environmentally friendly and support sustainability.
</p>

<p align=justify>
EzTrip aims to address these challenges by providing a solution based on artificial intelligence (AI). The app simplifies the travel planning process by offering more structured and relevant information. Key features such as personalized recommendations, expense tracking, an integrated automatic generate itineraries, and sentiment analysis from user reviews are designed to enhance the traveler experience and help them explore new destinations.
</p>

<p align=justify>
The app is also designed to support sustainable tourism by offering travel options that prioritize environmental friendliness and promote local culture to foreign tourists. Bali has been selected as the initial test destination due to its popularity among international tourists and its potential for implementing sustainable tourism concepts.
</p>

##### Business Objectives:
- Provide a well-organized, efficient, and eco-friendly travel experience by leveraging AI to deliver accurate and personalized recommendations.
- Increase engagement in the tourism industry by supporting the development of local destinations and promoting environmentally friendly tourism while showcasing local culture through personalized suggestions.
- Support sustainable tourism by offering travel options that consider environmental and social sustainability.
- Optimize the user experience by utilizing technologies like machine learning and image recognition to provide a responsive and relevant experience for every user.

##### Benefits for Stakeholders:
- **For Travelers**: Simplifies travel planning by providing easy access to relevant information, helping them discover unique and environmentally friendly travel experiences.
- **For the Tourism Industry**: Provides valuable data and insights to develop local destinations and introduce sustainable tourism options to global travelers.
- **For Destination Managers**: Utilizes collected data to improve infrastructure and tourism services, focusing on sustainability and enhancing the overall travel experience.

With EzTrip, travelers can not only plan their trips more easily and efficiently but also contribute to more responsible and sustainable tourism.

---

#### Data Understanding

The dataset used in this project is The [Bali Places Based On Category](https://www.kaggle.com/datasets/andreas7y/bali-places-based-on-category) dataset obtained from Kaggle, with `balieverything.csv` as the dataset used which was renamed to `tour.csv`. The Culinary dataset was obtained from TripAdvisor for [Restaurants in Bali](https://www.tripadvisor.com/FindRestaurants?geo=294226&offset=0&sort=FEATURED&establishmentTypes=10591&broadened=false) under the dataset named `culinary.csv`. Lastly, the `accommodation.csv` dataset was sourced from Traveloka for [Hotels in Bali](https://www.traveloka.com/en-en/hotel/indonesia/region/bali-102746).

##### ```Tour.csv``` Dataset Information

<div align=center>
  
| # | Column      | Non-Null Count | Dtype   |
|---|-------------|----------------|---------|
| 0 | name        | 312 non-null   | object  |
| 1 | rating      | 312 non-null   | float64 |
| 2 | category    | 312 non-null   | object  |
| 3 | price_wna   | 312 non-null   | float64 |
| 4 | city        | 312 non-null   | object  |
| 5 | address     | 312 non-null   | object  |
| 6 | google maps | 312 non-null   | object  |

</div>

<div align=center>
  
| Column        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `name`        | A column that shows the name of each tourist destination                     |
| `rating`      | A column that shows the rating of each tourist destination                   |
| `category`    | A column that indicates the category of each tourist destination             |
| `price_wna`   | A column that shows the entrance fee for foreigners to the tourist destination |
| `city`        | A column that indicates the city where the tourist destination is located   |
| `address`     | A column that shows the address of each tourist destination                  |
| `google maps` | A column that shows the link to the Google Maps location of each tourist destination |

</div>

##### Sample of ```Tour.csv```

<div align=center>

| name                   | rating | category           | price_wna | city     | address                                               | google maps                                                                                                                                                                                                              |
|------------------------|--------|--------------------|-----------|----------|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upside Down World Bali | 4.2    | Tourist attraction | 150000.0  | Denpasar | Jl. Bypass Ngurah Rai No.762                          | https://www.google.com/maps/place/Upside+Down+World+Bali/data=!4m7!3m6!1s0x2dd2414421ee552f:0xb23009c36c511835!8m2!3d-8.716711!4d115.2052612!16s%2Fg%2F11cl_3yx00!19sChIJL1XuIURB0i0RNRhRbMMJMLI?authuser=0&hl=en&rclk=1 |
| Alas Kedaton           | 4.2    | Tourist attraction | 50000.0   | Tabanan  | F5C4+644, Jl. Raya Alas Kraton                        | https://www.google.com/maps/place/Alas+Kedaton/data=!4m7!3m6!1s0x2dd23b164d2a8bb3:0x118812004a86244b!8m2!3d-8.5294825!4d115.1553403!16s%2Fg%2F1ptx26t72!19sChIJs4sqTRY70i0RSySGSgASiBE?authuser=0&hl=en&rclk=1           |
| Big Garden Corner      | 4.3    | Tourist attraction | 50000.0   | Denpasar | Sanur, Jl. Bypass Ngurah Rai                          | https://www.google.com/maps/place/Big+Garden+Corner/data=!4m7!3m6!1s0x2dd24071d99200c3:0x6b8b5fe4aa9162c0!8m2!3d-8.6568602!4d115.253657!16s%2Fg%2F11c0pyr1_h!19sChIJwwCS2XFA0i0RwGKRquRfi2s?authuser=0&hl=en&rclk=1      |
| Taman Nusa             | 4.3    | Museum             | 100000.0  | Gianyar  | Banjar Blahpane Kelod, Jl. Taman Bali Â– Banjarangkan | https://www.google.com/maps/place/Taman+Nusa/data=!4m7!3m6!1s0x2dd216dde1b8da09:0xd36ee4095fe3d8e6!8m2!3d-8.5286174!4d115.3585207!16s%2Fg%2F1hhvw85_q!19sChIJCdq44d0W0i0R5tjjXwnkbtM?authuser=0&hl=en&rclk=1             |
| Krisna Funtasticland   | 4.3    | Tourist attraction | 90000.0   | Buleleng | RXCV+HMR, Jl. Seririt- Singaraja                      | https://www.google.com/maps/place/Krisna+Funtasticland/data=!4m7!3m6!1s0x2dd18354c1674f11:0xeab10ee4e8cf7f1a!8m2!3d-8.1785032!4d114.9941258!16s%2Fg%2F11c20swxtm!19sChIJEU9nwVSD0S0RGn_P6OQOseo?authuser=0&hl=en&rclk=1  |

</div>

##### ```Culinary.csv``` Dataset Information

<div align=center>

| # | Column    | Non-Null Count | Dtype   |
|---|-----------|----------------|---------|
| 0 | name      | 664 non-null   | object  |
| 1 | rating    | 664 non-null   | float64 |
| 2 | category  | 664 non-null   | object  |
| 3 | price_wna | 664 non-null   | float64 |
| 4 | city      | 664 non-null   | object  |
| 5 | address   | 664 non-null   | object  |

</div>

<div align=center>

| Column        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `name`        | A column that shows the name of each culinary destination                     |
| `rating`      | A column that shows the rating of each culinary destination                   |
| `category`    | A column that indicates the category of each culinary destination             |
| `price_wna`   | A column that shows the price for foreigner to the culinary destination |
| `city`        | A column that indicates the city where the culinary destination is located   |
| `address`     | A column that shows the address of each culinary destination                  |

</div>

##### Sample of ```Culinary.csv```

<div align=center>
  
| name                                   | rating | category      | price_wna | city    | address                                                                              |
|----------------------------------------|--------|---------------|-----------|---------|--------------------------------------------------------------------------------------|
| Kabana Ubud By K Club                  | 5      | Bar           | 300000.0  | Gianyar | Jalan Raya Cebok, Tegalalang 80561 Indonesia                                         |
| Nautilus Seafood Restaurant & Bar      | 5      | Bar           | 300000.0  | Gianyar | Jl. Suweta No.80, Ubud, Ubud 80571 Indonesia                                         |
| MoonLite Kitchen and Bar               | 4.5    | Asian         | 300000.0  | Badung  | Jl. Abimanyu Jl. Dhyana Pura, Seminyak 80361 Indonesia                               |
| The Power of Love - Samabe Cave Dining | 5      | Seafood       | 500000.0  | Badung  | Jl. Pura Barong-Barong Sawangan, Nusa Dua, Benoa 80363 Indonesia                     |
| Koral Restaurant                       | 5      | International | 500000.0  | Badung  | Jl. Raya Nusa Dua Selatan The Apurva Kempinski Bali, Nusa Dua, Benoa 80361 Indonesia |

</div>

##### ```Accommodation.csv``` Dataset Information

<div align=center>

| # | Column    | Non-Null Count | Dtype   |
|---|-----------|----------------|---------|
| 0 | name      | 506 non-null   | object  |
| 1 | rating    | 506 non-null   | float64 |
| 3 | price_wna | 506 non-null   | float64 |
| 4 | city      | 506 non-null   | object  |

</div>

<div align=center>

| Column        | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| `name`        | A column that shows the name of each accommodation                     |
| `rating`      | A column that shows the rating of each accommodation                   |
| `price_wna`   | A column that shows the price for foreigner to the accommodation |
| `city`        | A column that indicates the city where the accommodation is located   |

</div>

##### Sample of `Accommodation.csv`

<div align=center>

| name                                | rating | price_wna  | city   |
|-------------------------------------|--------|------------|--------|
| The Anvaya Beach Resort Bali        | 4.45   | 5022000.0  | Badung |
| The Apurva Kempinski Bali           | 4.45   | 14520640.0 | Badung |
| The Sakala Resort Bali - All Suites | 4.25   | 2400000.0  | Badung |
| Discovery Kartika Plaza Bali        | 4.3    | 1733333.0  | Badung |
| Hilton Bali Resort                  | 4.35   | 3872000.0  | Badung |

</div>

---

#### Data Preparation and Preprocessing
This stage aims to prepare and process the data to be used for analysis and model training, ensuring it is relevant to the requirements. This involves removing unnecessary columns, cleaning missing values, and checking and removing duplicate data.
1. Removing Unnecessary Column<br>
In all three datasets, all columns are necessary for analysis and model training, so no columns were removed.
2. Checking for Missing Values<br>
The process of checking for missing values was conducted on each dataset `tour`, `culinary`, and `accommodation`. Based on the results, it was found that there were missing values in the `tour` dataset, leading to deletion in that dataset.
3. Checking for Duplicate Data<br>
In all three datasets, there are no duplicate data, so no correction or deletion  are necessary

---

#### Model Development

##### Neural Network
<p align=justify>
A simple neural network with 4 inputs, which are the content features and 1 output, which is the relevance score. The network consists of an input layer, 2 hidden layers, and an output layer. The network receives four numerical inputs, which are processed by the neurons in the hidden layer(s) using weighted connections and an activation function (ReLU). These weights are adjusted during training using backpropagation to minimize the error between the predicted output and the actual target values. The output layer then produces a single value, typically transformed by sigmoid activation function, which maps the result to a value between 0 and 1, representing a probability or score. The network is trained on labeled data, where the output score (0 or 1) is the target, and the objective is to minimize the prediction error over the training process.
</p>

##### Cosine Similarity
The cosine similarity between two vectors $$\( \mathbf{A} \)$$ and $$\( \mathbf{B} \)$$ is given by:

$$
\text{cosine similarity} = \frac{\mathbf{A} \cdot \mathbf{B}}{\|\mathbf{A}\| \|\mathbf{B}\|}
$$

Where:

- $\mathbf{A} \cdot \mathbf{B}$ is the dot product of vectors $\mathbf{A}$ and $\mathbf{B}$.
- $\|\mathbf{A}\|$ and $\|\mathbf{B}\|$ are the magnitudes (or Euclidean norms) of $\mathbf{A}$ and $\mathbf{B}$, calculated as $\|\mathbf{A}\| = \sqrt{A_1^2 + A_2^2 + \cdots + A_n^2}$ and similarly for $\|\mathbf{B}\|$.

The dot product $$\( \mathbf{A} \cdot \mathbf{B} \)$$ is computed as:

$$\mathbf{A} \cdot \mathbf{B} = A_1B_1 + A_2B_2 + \cdots + A_nB_n$$

This results in a cosine similarity score between $$\( -1 \)$$ and $$\( 1 \)$$.

<p align=justify>
A cosine similarity of 1 indicates that the vectors are identical (they have the same direction), 0 indicates orthogonality (no similarity), and -1 indicates opposite directions. This model is useful in the recommender system to show other content that is similar with content that we have already known.
</p>

##### Lexical Natural Language Processing
<p align=justify>
Lexical NLP helps by understanding the individual words in a review to determine whether the overall sentiment is positive, negative, or neutral. It looks at the words used and their meanings, including whether they are expressing strong emotions like "love" or "hate" or milder sentiments like "okay" or "fine". It also handles things like negations, for example "not happy" means the opposite of happy, and the intensity of sentiment like "very good" vs. "good". By analyzing the words and their relationships, lexical NLP helps identify the tone of the text and classify it into sentiment categories.
</p>

##### Manual Expenses Tracker
<p align=justify>
Manual expenses tracker offers six options for users to manage their spending. The first option, "Set a budget for today," allows users to define how much they plan to spend on a particular day. The second option, "Add expenses," enables users to input details about their expenses with their category (food & beverages, shopping, transportation, and others. "View my total spending today" shows users a summary of how much they have spent so far on the current day. The fourth option, "View my spending history," gives access to past spending records, helping users track trends over time. "Spending visualization" provides graphical representations to help users better understand their spending patterns. Finally, the "Exit" option allows users to close the tracker and end their session. This model is designed to offer a simple and organized way for users to control and monitor their daily expenses
</p>

#### Evaluation

##### Neural Network Model
<div align=center>
  <img src="https://github.com/user-attachments/assets/989d6462-179f-4f60-863e-73e6f56c6371"/>
</div>
<p align=justify>
With 150 epochs, the model training results were quite good. From the loss curve, it can be seen that there is a decrease, which means that the model is learning and improving its performance to decrease the error. The smaller validation loss compared to training loss also means that the model is not overfitted.
</p>

<div align=center>
  <img src="https://github.com/user-attachments/assets/6ca8d0e2-be4a-4104-8fb9-2c215199adbe"/>
</div>
<p align=justify>
From the RMSE curve, it can be seen that the RMSE is 23%. This means that the accuracy obtained from the model is around 77%. Even though at the beginning of the epoch there was a decline, after that the RMSE only fluctuated. Validation RMSE is also lower than training RMSE.
</p>

<div align=center>
  <img src="https://github.com/user-attachments/assets/593776fa-834b-4e7c-a500-57b0d62cc062"/>
</div>
<p align=justify>
With the tourist attraction category, Badung City, minimum rating of 4.5, and maximum price of IDR 40.000, the output of the model can be seen in the image above.
</p>

##### Cosine Similarity
<div align=center>
  <img src="https://github.com/user-attachments/assets/e4e68bef-4135-4ca8-bd6c-54e13c9d00b2"/>
</div>
<p align=justify>
For the cosine similarity model, very good results were obtained. It can be seen from the output image above, by entering the 5GX Bali, which is a tourist attraction in Badung with an entrance ticket price of Rp 30.000, user are given the top 5 similar places with a similarity of almost 1, which is very good in terms of this model. It can be seen that the city and place categories are the same as the input.
</p>

##### Lexical Natural Language Processing
<div align=center>
  <img src="https://github.com/user-attachments/assets/e62829b9-c7c8-46eb-b197-0ffd502faada"/>
</div>
<p align=justify>
For the lexical NLP model, the results obtained are also quite good. The image above is just an example for user input and output. The model can detect languages ​​other than English by translating them first. However, the disadvantage of this model is that there is the possibility of translation errors and lexical NLP cannot find the implied meaning of the review, such as sarcasm. For example the second review the sentiment should be neutral or positive, but the result is negative.
</p>

---

#### Contributing

<div align=center>

| Name  | Bangkit ID | Roles | University | Work Branch |
|---|---|---|---|---|
| Marvin Wijaya | M002B4KY2421 | Machine Learning Engineer | Institut Teknologi Bandung | [Clicke here!](https://github.com/C242-PS269/eztrip-machine-learning/tree/ml-branch-1) |
| Shionita Dwilani Nainggolan | M002B4KX4144 | Machine Learning Engineer | Institut Teknologi Bandung | [Click here!](https://github.com/C242-PS269/eztrip-machine-learning/tree/ml-branch-2) |
| Irvan Hartawan | M002B4KY2010 | Machine Learning Engineer | Institut Teknologi Bandung | [Click here!](https://github.com/C242-PS269/eztrip-machine-learning/tree/ml-branch-3) |

</div>

#### License

<p align=justify>
There is <b>NO LICENSE</b> available yet as this project is still being used for purposes that cannot be published as open source, therefore please read the disclaimer section.
</p>

#### Disclaimer

- This project is currently part of the <a href="https://www.dicoding.com/programs/bangkit">Bangkit Academy led by Google, Tokopedia, Gojek, and Traveloka</a> program and is being developed by our team as part of the Capstone Project.
- The primary purpose of this project is to fulfill the requirements of the <b>Bangkit Academy 2024 Batch 2</b> program and to demonstrate the technical and collaborative skills we have acquired during the program.
- The project is not yet intended for open-source release or commercial use. All rights and restrictions related to the project remain under the team's discretion until further notice.

---

#### Author

Github Organization: [EzTrip - C242-PS269 Capstone Team](https://github.com/C242-PS269)
