# 11_05_ASSI_Propose_a_normalization_problem
## Authors  
- **Kevin Coaquira Choquecallata**  
- **Sami Said Benyacoub Manseur**  

## Normalization  
The objectives of standardization are the following:  
- Have stored with as little space as possible.  
- Delete duplicate data.  
- Eliminate logical errors.  
- Sorted data.  

There are several normal ways but here we are only going to do the first 3 which are:  
- First Normal Form(1FN).  
- Second Normal Form(2FN).  
- Third Normal Form(3FN).  

We will take as reference the Team table created in the previous work with following extra attributes:  
- **id**
- name_team
- ciudadFundada
- name_player  
- position
- nameStadium  
![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/39037ec1-9acc-4526-bc24-3fda2352267a)  
## 1FN (**FIRST NORMAL FORM)**  
- Each table cell must contain a single value.  
- Each record must be unique.  

Here we see all the cells must have a unique value, we see that several names are repeated in the namePlayer column, because what we do is create a new separate row and insert so that each cell is a unique name. This happens the same in the Position column. 
![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/a9dbf4c8-36c2-4591-93b1-1c400037d20a)  
## 2FN (**SECOND NORMAL FORM**)  
- Rule 1- Be in 1NF.
- Rule 2- Single Column Primary Key.  

Once you have 1FN, we check that it has a complete primary key. We divide into 2 tables and see that the primary key is id and in the other table we have it as FK called id_team.  
![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/03a87de1-e648-4f3e-9964-213733b5ccf4)  
![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/f4e9f954-7e51-4f0e-8a0f-7b252788fb38)  

## 3FN (**THIRD NORMAL FORM**)  
- Rule 1- Be in 2NF.
- Rule 2- It does not have transient functional dependencies.  

Once you have 1FN and 2FN, we check that it does not have transitive dependencies, that is to say that the attributes do not depend on a primary key but their primary key is found in the same table.  
The Stadium column is linked to the cityFounded not the team name.  

![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/2a11fefd-3bde-45a1-a940-612181bf6ec2)  
![image](https://github.com/sami24120/11_05_ASSI_Propose_a_normalization_problem/assets/91737963/05782b91-c13a-48f4-bd49-64852333d710)


