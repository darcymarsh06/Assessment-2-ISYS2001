
My financial assistant works to give the user a tracking of how they are going in achieving their saving goal for the year by collecting their yearly income, monthly expenses and saving goal to then compile and calculate if they will reach their goal. The assistant will use lists and dictionaries to rank their expenses from most to least expensive to give clearer results to the user. The code also creates a CSV of the listed expenses that it will search for when the user re-runs the code and apply to save their previous entries. 
The assistant will then use and API to Google GenAI 3.8 flash to give feedback personalised to the users results and give then unique, friendly and educational tips to improve upon their findings. 

The sample input:

<img width="468" height="497" alt="image" src="https://github.com/user-attachments/assets/427f9692-3877-4611-a90d-4cf71af42bb4" />


The sample output: 

Expenses Ranked (Highest to Lowest):
Rent: $1,200.00 per month ($14,400.00 yearly)
Groceries: $450.00 per month ($5,400.00 yearly)
Entertainment: $400.00 per month ($4,800.00 yearly)
Utilities: $300.00 per month ($3,600.00 yearly)
Food: $300.00 per month ($3,600.00 yearly)
Financial Statistics & Goal Tracking
Yearly Income: $50,000.00 Total Monthly Expenses: $2,650.00 Total Yearly Expenses: $31,800.00 Projected Remaining: $18,200.00 Your Savings Goal: $10,000.00

Congratulations darcy! You are on track to meet your savings goal with a surplus of $8,200.00!

Personalised AI Suggestions:
Hi Darcy! First off, give yourself a huge pat on the back—you’re in a fantastic financial position. With $18,200 left over after expenses, you have plenty of breathing room to crush your $10,000 savings goal and then some!

Here are a few friendly tips to make the most of your money this year:

- Put your $10,000 goal on autopilot: To hit your goal effortlessly, set up an automatic monthly transfer of about $834 into a High-Yield Savings Account (HYSA). Automating it right after payday means you’ll reach your target by the end of the year without even having to think about it!

- Put your surplus to work: Even after hitting your $10,000 goal, you still have about $8,200 in wiggle room. Consider funneling some of this extra cash into long-term growth—like opening or maxing out a Roth IRA—or building a solid 3-to-6-month emergency fund if you don’t already have one.

- Enjoy your healthy budget balance: Your rent ($1,200/month) sits right around 29% of your income, which hits the golden rule of keeping housing costs under 30%. Since your essentials are so well-balanced, make sure to carve out a small "fun fund" each month so you can enjoy your hard-earned money guilt-free.
You’re doing an amazing job, Darcy—keep up the great momentum!


How it runs: 

1. The Colab first uploads the GenAI library and then installs and upgrades the Gradio interface which is then imported with the pandas and CSV.
2. the genai API key is first linked into the code.
3. The CSV file is checked to see if user has previous saved data or it continues to collect it as usual
4. then we define the variables we are collecting to create the strings and objects
5. we then set the income range parameters with the if then actions to inform the user if its out and what the parameters are
6. then the expense list entry collection section is formated.
7. the entries are then sorted from highest to lowest using lambda
8. the expenses are then auto saved to the users CSV file
9. The calculations are then done on the entries to create the output results
10. the ranked expenses are then formatted
11. the output is further formatted with the strings we created earlier for each variable we are collecting.
12. Then the pre-written response of either reached savings goal or not
13. Now the GenAI API is included with prompts on what objects to respond to how how to respond
14. then the Grado interface is built with the themes and formatting.
15. And now the code runs.
