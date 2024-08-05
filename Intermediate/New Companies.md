# New Companies

#### Amber's conglomerate corporation just acquired some new companies. Each of the companies follows this hierarchy:

![Hierarchy](https://github.com/user-attachments/assets/2c21f37e-fbe9-4fe5-9612-48709e3826cd)

#### Given the table schemas below, write a query to print the company_code, founder name, total number of lead managers, total number of senior managers, total number of managers, and total number of employees. Order your output by ascending company_code.

#### Note:
#### - The tables may contain duplicate records.
#### - The company_code is string, so the sorting should not be numeric. For example, if the company_codes are C_1, C_2, and C_10, then the ascending company_codes will be C_1, C_10, and C_2.

---

#### Input Format

#### The following tables contain company data:

#### Company: The company_code is the code of the company and founder is the founder of the company.

![Company](https://github.com/user-attachments/assets/64fa5efe-207a-46ed-9c73-a20949cff092)

#### Lead_Manager: The lead_manager_code is the code of the lead manager, and the company_code is the code of the working company.

![Lead_manager](https://github.com/user-attachments/assets/514c3fcf-cdf0-4d4c-b4ed-03725ae2f379)

#### Senior_Manager: The senior_manager_code is the code of the senior manager, the lead_manager_code is the code of its lead manager, and the company_code is the code of the working company.

![Senior_Manager](https://github.com/user-attachments/assets/3a430998-33d9-4e49-afa7-63b96f59f2d2)

#### Manager: The manager_code is the code of the manager, the senior_manager_code is the code of its senior manager, the lead_manager_code is the code of its lead manager, and the company_code is the code of the working company. 

![Manager](https://github.com/user-attachments/assets/d81ee54d-3c29-4554-b8c1-93db3c32041d)

#### Employee: The employee_code is the code of the employee, the manager_code is the code of its manager, the senior_manager_code is the code of its senior manager, the lead_manager_code is the code of its lead manager, and the company_code is the code of the working company.

![Employee](https://github.com/user-attachments/assets/92f712b2-6e39-45bc-93df-947350049ecf)

---

#### Solution:-
```
SELECT
         Company.company_code,
         founder,
         COUNT(DISTINCT Lead_Manager.lead_manager_code) AS LM_count,
         COUNT(DISTINCT Senior_Manager.senior_manager_code) AS SM_count,
         COUNT(DISTINCT Manager.manager_code) AS M_count,
         COUNT(DISTINCT Employee.employee_code) AS Emp_count
FROM
         Company 
         JOIN Lead_Manager ON Company.company_code = Lead_manager.company_code
         JOIN Senior_Manager ON Lead_Manager.lead_manager_code = Senior_Manager.lead_manager_code
         JOIN Manager ON Senior_Manager.senior_manager_code = Manager.senior_manager_code
         JOIN Employee ON Manager.manager_code = Employee.manager_code
GROUP BY 
         Company.company_code,
         founder
ORDER BY
         Company.company_code;
```
#### Using ```JOIN``` operator the given tables were joined and using ```COUNT``` function the number of lead managers,senior managers,managers and employees were counted.

            
