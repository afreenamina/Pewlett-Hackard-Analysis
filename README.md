# Pewlett-Hackard-Analysis

## Overview of the analysis:

The analysis is for Pewlett Hackard - a large company boasting several employees, as they have several employees retiring in near future, so the below two new analysis is done for future-proofing the company -

 * The number of retiring employees per title - By determining the number of employee titles, the company can soon open the position and start recruiting based on the position titles.
 
 * Employees who are eligible to participate in a mentorship program - By calculating the eligibility, we can start the knowledge transfer to the next employee/new recruit to retain vital knowledge that employee has learned over the course of their careers.

## Results: 

### The number of retiring employees per title :

Below are the steps performed to find number of retirement-age employees per title

* First we will get the number of retirement-age employees by filtering the data by Birthdate of employees who were born between 1952 and 1955.
  Below is the SQL code to retrieve the data -
  
  ![1](https://user-images.githubusercontent.com/92698873/145701030-d491d414-c0e7-4562-a3e5-318c20f829fb.png)
  
* As some employees have multiple titles in our data, to get the latest title of each employee, we use DISTINCT ON in SQL query.

![2](https://user-images.githubusercontent.com/92698873/145701039-81061727-3d7c-4946-9573-11b866cae105.png)

* COUNT() and GROUP BY function was used to find the number of retirement-age employees by there title.

![3](https://user-images.githubusercontent.com/92698873/145701157-3833cd8c-364b-4ac6-b8eb-ab2742ee2f4d.png)


### Mentorship program eligiblity :

* Three different table - employees table, dept_emp table and title table has been joined using JOIN and filtered by BirthDate to get the number of employees who are eligible for mentorship program.

* Below is the SQL code for the query.

![Screenshot 2021-12-11 211447](https://user-images.githubusercontent.com/92698873/145701253-0ad14218-1ed0-4874-9412-3be8bbc19f9d.png)

##Summary: 

### The number of retiring employees per title :

* Below is the final output data of retiring employees per title -

![4](https://user-images.githubusercontent.com/92698873/145701228-0cf9cec1-2cfb-4648-8ce9-d2fc53882c32.png)

* From the results, there are 90398 employees comes under silver tsunami list.

* As the list seems to be huge, we can further break down by sorting the retiring employees based on the department and the list can be sent to each department managers and they can decide on next steps.
     * For the Department - Quality Management, we have total of 6136 retiring employees
     
    ![qualitymanaq](https://user-images.githubusercontent.com/92698873/145705430-48d553ac-77d4-4126-b710-483899b1b254.png)
    ![qualitymanaqcount](https://user-images.githubusercontent.com/92698873/145705432-bf12639b-ed79-4717-a6f2-7de59628d7e0.png)

     * For the Department - Marketing, we have total of 6047 retiring employees
  
    ![marketingq](https://user-images.githubusercontent.com/92698873/145705497-881d80ac-6cd3-4d07-a6df-a500fae58834.png)
    ![marketingqcount](https://user-images.githubusercontent.com/92698873/145705500-5cc32d4b-df43-41ab-99bf-c1c96246f5e4.png)

    * This can be repeated for other departments 
    
    ![image](https://user-images.githubusercontent.com/92698873/145705522-a251394d-bf79-4db2-98c5-7db46dc352e8.png)

### Mentorship program eligiblity :

* Below query used for getting title count of employees eligible for mentorship program.

![5](https://user-images.githubusercontent.com/92698873/145703761-e294d511-eb35-45bf-954f-7353499aee9b.png)
![5_1](https://user-images.githubusercontent.com/92698873/145703762-5a5e2b53-16c6-4d63-99da-830f7c187eb7.png)

From this data we can check if the company needs the position to be replaced/promoted by current employee or it needs a new recruit.Once they have a replacement for the current employee, they can start the mentorship program.

 
