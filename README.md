# Northwind Services: Organization Design

## Group Design

Northwind uses security groups to organize users by department and job function. I used the naming convention `SEC-<Type>-<Name>` so each group's purpose is immediately clear.

 Group                  Why it exists                                                                                                        

- `SEC-Dept-Executive`  Identifies the company's executive user and provides a clear department boundary for future executive access.        
- `SEC-Dept-IT`          Groups employees working in IT, including the IT Manager, Systems Administrator, and Help Desk Technician.           
- `SEC-Dept-Finance`     Groups employees responsible for finance, payroll, and invoicing so finance-related access can be managed centrally. 
- `SEC-Dept-Sales`       Groups Sales employees so Sales-related access can be managed through one group rather than individual accounts.     
- `SEC-Dept-HR`          Groups HR employees responsible for employee administration, onboarding, and offboarding.                            
- `SEC-Dept-Contractors` Separates external contractors from employees so their access can be identified and reviewed independently.          
- `SEC-Role-Helpdesk`    Identifies users with Help Desk responsibilities regardless of their department.                                     

## Why Department Groups

I grouped users by department because Northwind is a small organization and department membership provides a simple, understandable way to organize people and manage access. It also avoids assigning access directly to individual users.Employees in the same department can have different responsibilities, applications, and privilege levels. This is why I also created the `SEC-Role-Helpdesk` group to represent a job function separately from the IT department.

## Contractor Decision

I placed contractors in `SEC-Dept-Contractors` rather than treating them exactly like regular employees. Contractors are external workers with fixed end dates, so separating them makes their accounts easier to identify and review. Their access should be removed or their accounts disabled when their contracts end.

## Scaling to 500 People

With 500 users, I would keep the department structure but introduce dynamic group membership using attributes such as department and job title, where the appropriate Entra licensing is available. I would automate joiner, mover, and leaver processes and establish periodic access reviews to reduce manual administration and stale access.

## What I Got Wrong and Fixed

During the build, I found inconsistent department values such as `Finanace`, `Sales Staff`, `HR staff`, and `Contractor`. I corrected them to `Finance`, `Sales`, `HR`, and `Contractors` so the directory uses consistent department values. I also had issues determining the domain name for each username/group. Lol, this took me 1 hour to figure it out.
I also initially used simple group names such as `Finance`. I corrected them to follow the agreed naming convention, such as `SEC-Dept-Finance`. This reinforced the importance of establishing naming standards before creating directory objects, because correcting inconsistent naming becomes more difficult as a directory grows.


[!image alt](https://github.com/LarisaDuru/entra-directory-foundation/blob/45ff33806f83dbf3a882e25b6320ece2806db39c/screenshots/UsersTemplate.csv)

