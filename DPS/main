

import numpy as np
import pickle as pi
import streamlit as sl


loaded_model = pi.load(open("C:\Users\OneDrive\Desktop\code\Multiple_D\trained_model.sav", 'rb'))


def diabetes_prediction(input_data):
    
    
    numpy_input = np.asarray(input_data)

   
    input_reshaped = numpy_input.reshape(1,-1)


    prediction = loaded_model.predict(input_reshaped)

    if(prediction[0] == 0):
        return 'The person is non diabetic'
    else:
        return 'The person is diabetic'
    

def main():
    
    sl.title('Diabetes Prediction')
    
    p = sl.text_input('Number of Pegnancies')
    g = sl.text_input('Glucose Level')
    bp = sl.text_input('Blood Pressure Value')
    st = sl.text_input('Skin Thickness Value')
    i = sl.text_input('Insulin Level')
    BMI = sl.text_input('BMI Value')
    dpf = sl.text_input('Diabetes Pedigree Function Value')
    a = sl.text_input('Age of the Person')
    
    diagnosis = ''
    
    if(sl.button('Diabetes Test Result')):
        diagnosis = diabetes_prediction([p, g, bp, st, i, BMI, dpf, a])
        
    sl.success(diagnosis)
    
    
if __name__ == '__main__':
    main()
