# Northwind Services  Entra Directory Foundation

## Project Overview

This project demonstrates the design and setup of Nothwind's identity directory using Microsoft Entra ID. The goal was to create a structured directory where users can be organized and access can eventually be managed through security groups instead of individual users.

## Business Scenario

Northwind Services is a fictional 15-person company moving from shared logins and spreadsheets to Microsoft Entra ID.

The company has employees across:
- Executive
- IT
- Finance
- Sales
- HR
- Contractors

The sales employees was later expanded to include a fifth salesperson, bringing the total to 16 Northwind users.

## Tools Used

- Microsoft Entra ID
- GitHub
- Screenshots for documentation and evidence

## What I Built

- Created Northwind user accounts in Microsoft Entra ID
- Created department-based security groups
- Created a role-based `SEC-Role-Helpdesk` group
- Added users to the appropriate groups
- Applied consistent department values
- Established a security group naming convention
- Documented the directory design and contractor approach
   Compared group-based access with individual access assignments

### Security Groups

 Group                   Purpose                               

- `SEC-Dept-Executive`   Executive users                       
- `SEC-Dept-IT`          IT employees                          
- `SEC-Dept-Finance`     Finance employees                     
- `SEC-Dept-Sales`       Sales employees                       
- `SEC-Dept-HR`          HR employees                          
- `SEC-Dept-Contractors` External contractors                  
- `SEC-Role-Helpdesk`    Users with Help Desk responsibilities 

## Screenshots

The project includes screenshots showing

1. Northwind users in Entra ID
2. Individual user details
3. Security groups and naming convention
4. Group membership
5. Audit log activity

Screenshots are stored in the `screenshots` folder.

## Security Lessons Learned

Group-based access is easier to manage and review than assigning access individually to every user.
I also learned that contractors should be handled deliberately because they are external workers with fixed end dates. Separating contractors from employees makes their access easier to identify and review.

Consistent naming and department values are also important because inconsistent directory data becomes harder to manage as the organization grows.

## Future Improvements

If Northwind grows, I would:
- Introduce dynamic group membership where appropriate
- Create additional role-based groups
- Automate user creation 
- Implement regular access reviews
- Improve joiner, mover, and leaver processes
- Export audit logs for longer-term retention
- Develop a more formal access governance process
This project demonstrates that identity management is not just about creating users. The directory needs a structure that makes access understandable, manageable, and scalable. The group design, naming standards, contractor handling, and documentation were created with that goal in mind.
