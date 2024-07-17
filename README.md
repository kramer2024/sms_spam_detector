# sms_spam_detector
AI camp module 21 challenge

# Background
You'll be refactoring code from an SMS text classification solution into a function that constructs a linear Support Vector Classification (SVC) model. Once the model is created and trained, you will create a Gradio app to host the application, enabling users to test text messages. The application will provide feedback to users, indicating whether the text is classified as spam or not, based on the model's performance.

# Create the SMS Classification Function
Using the code in the sms_text_classification_solution.ipynb file, create the sms_classification function in the gradio_sms_text_classification.ipynb by doing the following: Set the features variable to the text message column of the DataFrame. Set the target variable to the "label" column of the DataFrame. Split data into training and testing and set the test_size to 33%. Build a pipeline to transform the test set to compare to the training set. Fit the model to the transformed training data and return model. Load the SMSSpamCollection.csv into a DataFrame and call the sms_classification function with the DataFrame, and set the result to the "text_clf" variable.

# Create the SMS Prediction Function
Use the sms_prediction function to predict the classification of a new text by doing the following: Create a variable that will hold the prediction of a new text. Use a conditional statement that determines if the text message is "ham" or “spam”. 
If the message is “ham”, the function should return the following message: f'The text message: "{text}", is not spam.'

If the message is spam, the function should return the following message: f'The text message: "{text}", is spam.'

# Create the Gradio Interface Application
Create a Gradio Interface application that takes a textbox for the inputs and has a textbox for the output. The textboxes should have labels that describe what each textbox contains.

# Launch and test the application 
Test the following text messages with the application: 

1. You are a lucky winner of $5000!
    result: 'Ham'
2. You won 2 free tickets to the Super Bowl.
    result: 'Ham'
3. You won 2 free tickets to the Super Bowl. Text us to claim your prize.
    result: 'Spam'
4. Thanks for registering. Text 4343 to receive free updates on medicare.
    result: 'Spam'