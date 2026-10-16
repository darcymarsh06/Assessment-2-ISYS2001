The first step in making my finance assistant was determining the function I wished it to have for its user. I wanted my code to give its users insight into how they were tracking towards reaching their savings goal for the year to help motivate them towards it and give support and advice based on the findings. 

For my first part I uploaded the Gradio interface for my program to the Colab. Then I practiced the code to test how Gradio would run. 

 <img width="290" height="130" alt="image" src="https://github.com/user-attachments/assets/a8ce0fa4-a4f0-4eb5-bb5f-9edb6db7de46" />


Then I practiced the basic entry input and output sections of code to also begin setting the parameters for what the max and min could be for yearly income. 

<img width="451" height="162" alt="image" src="https://github.com/user-attachments/assets/dbce94a6-e745-4e40-9dc2-4154d77363dd" />
 

Now I wrote my first prompt for Google Gemini to create a base code for me to alter and edit 
My prompt: 
Write a python code for a personable financial assistant that is helping the user track their saving goal. It needs to ask their name, welcome them then use loops to ask their yearly income min $1000 max $1000000 then log their average monthly spending through getting them to list the items and prices then calculate it to be yearly and provide them with statistics on how they are going on reaching their savings goal for the year and make some suggestions if they need to cut down or support if they are on track.

This first prompt gave me a good base for my code. I then incorporated the Gradio interface and edited to outputs to be personalised to how I wanted to interact with the user. 
In this initial code I was also using loops for each of the data inputs which I then replaced parts of with pandas in my final code. 

 <img width="451" height="205" alt="image" src="https://github.com/user-attachments/assets/67daa658-31e8-4649-b752-51eaab7d5ff8" />

I then made sure the calculations section was written right and calculated the results I wanted to be displayed to the user. 
Then it was the sorting section for expenses into most to least expensive which Gemini used the key=Lambda function to rank by cost. 
I then wrote out the personalised suggestions for if they were within their savings goal and else for if they didn’t reach it. I ended up replacing this section when I added the Google Studio API Gen AI to create individual unique advice and responses to the users input. 

 <img width="451" height="121" alt="image" src="https://github.com/user-attachments/assets/4c030034-5968-41df-8b28-78f729568826" />


This initial code had errors when I came to ranking the items by cost as I had no correctly defined monthly_expense in the dictionary as when I combined my code with Geminis section they had defined it as expense_history. This shows something you need to be careful of when collaborating with AI for the code. I used the Colab built in gemini to find and correct this error. 

 <img width="451" height="173" alt="image" src="https://github.com/user-attachments/assets/9688f9ef-0353-4595-bb11-b8454a820f91" />


I then added the Gradio interface section to this code, which I had previously uploaded to my Colab. I used Gemini and our previous class codes to create this formatting section.

During the first code run the monthly expense section that Gemini created was not ideal as it had a set number and names for the expenses rather than a more adaptable and versatile section that can accommodate any amount of monthly expenses so in my final code, I adjusted it to fit any amount. 
 
   <img width="451" height="125" alt="image" src="https://github.com/user-attachments/assets/021c54cd-361f-458a-964c-de76337b7f47" />
<img width="451" height="155" alt="image" src="https://github.com/user-attachments/assets/c60025a9-67cc-4f80-93c7-f1efd26b50da" />



The code uses a series of strings to define each section of user data that will be inputted then with the input it creates an object string for the variable so that is can be analysed for the final outputs. You can keep track of the string sections by putting str at the end of the variable you are coding for. 

 <img width="451" height="189" alt="image" src="https://github.com/user-attachments/assets/aeacfabe-b69c-41c6-b04d-60f315b6d86e" />


Next, I implemented the pandas library by importing it at the start of the code and using it sort my data and store the CVS.

I chose to use the CVS data and file uses in 2 ways. When a user first inputs their data it will save as my_expenses to the colab and then when they return to the code and rerun it it will check for any previous saves CVS to auto input their saved data. It will then use the panda to read it. 
 
<img width="451" height="180" alt="image" src="https://github.com/user-attachments/assets/a0b0619d-41aa-44bb-85a8-21f9b2c2ea3c" />

The pandas also replace the coding for ranking the expenses to make it simpler

 <img width="451" height="152" alt="image" src="https://github.com/user-attachments/assets/08d871c4-db0e-479f-8233-1567cd2259d9" />


I also incorporated an API to integrate with Google Gen AI for personalised feedback on results at the end, giving my financial assistant more tailored use for its users. This took a few goes because first the API Key wasn’t linking properly with the code then it version of GENAI was not compatible for my code then finally the version 3.8 flash worked. 
The prompts made sure the AI was friendly, encouraging and informative. 
 
<img width="451" height="196" alt="image" src="https://github.com/user-attachments/assets/c883f1a7-174d-47d8-b68d-3600b16d663c" />

The first full run of code came up with a lot of errors with my main ones being indentation errors.

 <img width="451" height="109" alt="image" src="https://github.com/user-attachments/assets/ccaeefc1-9ef8-431a-8e70-bf11fcb65adf" />


Another error I encountered was that my IF function wouldn’t highlight purple, showing it was working, which turned out to be happening because I hadn’t closed the previous lines, so it was still building the string. 

Now that my full code is complete, I've run many tests to make sure it can handle input errors and different user scenarios.
-	I tested an income of over $1000000 and it comes up with error and gives the user the parameters
-	Then I tested the CSV data saving to make sure it remembers your previous expenses which worked right
-	 I then tried lots of different entry combinations to make sure the outputs were correct and educational. 

In my testing I also had the Error notification for incorrect Syntax but I hadn't altered my code so I corrected this by re-running the program from the beginning including reloading the gradio and genai uploads and this corrected it. 

<img width="602" height="217" alt="Screen Shot 2026-10-16 at 9 31 41 am" src="https://github.com/user-attachments/assets/44428d3c-d4a4-4f14-a30f-b8470467a577" />
