![head image](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/f606bf96-ba1f-474d-9524-a2f6bd33fe6a)

# 📢 ChurnPredict Pro: Customer Churn Prediction App with Gradio💥🔍

In today's competitive business landscape, understanding and predicting customer behavior is paramount. One crucial aspect of this is forecasting customer churn, which can help businesses make data-driven decisions to enhance customer retention and satisfaction. ChurnPredict Pro is a cutting-edge web application that leverages the power of machine learning, specifically a Random Forest Classifier model, to provide real-time customer churn predictions. 

This article takes you on a journey through the development process of ChurnPredict Pro, highlighting the technology stack, features, and the exciting journey of integrating machine learning models for accurate churn predictions.

## Introduction

ChurnPredict Pro is an innovative web application designed to predict customer churn.  The application allows users to input customer data effortlessly and receive instant churn predictions, thereby enabling them to take proactive measures to retain valuable customers.

## The Importance of Customer Churn Prediction

Customer churn, the loss of customers, can have a significant impact on a company's bottom line. By predicting churn, businesses can take preventive actions, such as targeted marketing and improved customer service, to reduce customer attrition. This predictive power can lead to higher customer satisfaction, improved profitability, and a more sustainable business model.

## The Technology Stack

ChurnPredict Pro relies on a robust technology stack to deliver real-time customer churn predictions. Here are the key technologies used in the development of the application:

- Gradio: A Python library for building interactive interfaces, which is the foundation of the user interface.

- Pandas: A widely used library for data manipulation and analysis.

- Scikit-Learn: A machine learning library that simplifies the implementation of various machine learning algorithms.

- Joblib: Used for serialization and deserialization of machine learning models.

## Development Process

1. ### Data Collection, Preprocessing and Model Training

The development of ChurnPredict Pro began with data. Historical customer information used in the previous project titled "📢 Unlocking Insights: Decoding Telecommunication Customer Churn Through Machine Learning!💥🔍" was used as the basis for training a Random Forest Classifier model. This data included various customer attributes, such as gender, senior citizen status, contract details, and payment method, which are used to make predictions about churn. The Random Forest Classifier is chosen because it emerged as the best performing model to handle churn prediction.

2. ### Preprocessor and Model Exports

The preprocessing steps and the Random Forest Classifier model were exported from the notebook using Joblib. This ensured that the preprocessor and model were readily available for further preprocessing tasks and forecasting within the app.
![prep 1](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/83a0f8e1-d063-41e3-a592-39d77edeab45)
![prep 2](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/70acd62b-d75f-469c-9923-131abc0c915b)

3. ### Building the User Interface

The user interface serves as the front end of ChurnPredict Pro. Built with Gradio, it offers an interactive and intuitive experience. The design allows users to effortlessly input customer data, and with a single click, receive real-time churn predictions.

Using Gradio Blocks, app's structure is organized into 2 main elements:

The main function responsible for the preprocessing of the input data and returning the churn prediction and the customer information in a DataFrame.

The output which consist of two components responsible for displaying the prediction and customer information.

The UI is composed of Rows and Columns for Layout and gradio components to receive the inputs from the user.

![app header](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/f8f75691-3f04-423a-a447-7e6239daea63)
![more cus info](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/f976061a-5f9f-4361-b2f1-ca0d3ab452d3)
![submit and pred](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/a0d7ca84-2741-4cd8-9a43-ff605cfe41e7)

4. ### Building the Logic

Upon submission of customer data, the submit button calls the churn_predict function and passes the customer data as input to the function.

![submit code](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/e30c8755-c7a9-46b6-9334-8a75d3cfaf01)
![func](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/6708068a-c7b9-436a-9e0c-a8683d669f61)

The churn_predict function is invoked, which initiates the data processing as follows:

- The preprocessor and model are loaded using joblib.load from the model files. These components are essential for making churn predictions.

- Customer data (received through *args)  is converted into a DataFrame.

- The categorical feature "SeniorCitizen" data is converted from "Yes"/"No" to "1"/"0" for machine learning compatibility.

- The preprocessor is applied to transform the user's input.

- Predictions are made using the Random Forest Classifier model.

- The DataFrame of the customer data and the predicted churn status is returned from the function.

![code on output](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/c1e6bc74-d700-433f-9a48-b3d0d067ba47)

The output is displayed in a user-friendly format, the Gradio Dataframe component displays the Customer Information as received from the user, and the Gradio Label component displays the prediction making it easy for businesses to understand the likelihood of churn and make informed decisions to retain customers.

5. ### Displaying Results

A simple click on the "Submit" button delivers a real-time churn prediction.

![pred](https://github.com/snyamson/P4-ChurnPredict-Pro/assets/58486437/037aae69-f99b-4a36-97f7-d99b9c535626)

ChurnPredict Pro simplifies churn prediction. With real-time predictions, businesses can take immediate actions to enhance customer retention. The application provides a clear prediction of whether a customer is likely to churn or stay, helping businesses plan their customer management strategies effectively.

## Conclusion

ChurnPredict Pro is more than a churn prediction tool; it's a solution that empowers businesses to optimize customer management. The development process involved data collection, model training, and the creation of an interactive user interface. ChurnPredict Pro exemplifies the potential of machine learning in real-time decision-making. Businesses can now anticipate customer churn and take the necessary steps to enhance customer satisfaction and profitability.

The journey of developing ChurnPredict Pro is a testament to the power of combining machine learning and user-friendly applications. With the ability to predict customer churn, businesses can stay ahead of the competition and deliver the best possible service to their customers.
