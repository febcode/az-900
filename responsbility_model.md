# Shared responsibility model
- The shared responsibility model applies to all the cloud service types.

- Depending on the configuration, you or the cloud provider may be responsible for networking settings and connectivity within your cloud environment, network and application security, and the directory infrastructure.

- M = Microsoft
- C = Customer
- S = Shared 

| Type                                       | Responsbility        | SaaS | Paas| IaaS| On-prem |
|-------------- -                            |---------------       |------|------|----|----------|
|Responsisbilty always retainred by custmoer | Information and Data | c    | c    |c    | c       |
|Responsisbilty always retainred by custmoer | Devices mobile and pc  | c    | c    |c    | c     |
|Responsisbilty always retainred by custmoer | Devices mobile and pc  | c    | c    |c    | c       
|Responsisbilty always retainred by custmoer | Idemtity and directory structure | S | S | c | c |
|Responsisbilty varies by type | Applications | M | S | c | c |
|Responsisbilty varies by type | Network control | M | S | c | c |
|Responsisbilty varies by type | Operating szystem | M | M | c | c |
|Responsisbilty transfer to cloud Provider  | Physical Hosts | M | M | M | c |
|Responsisbilty transfer to cloud Provider  | Physical Network | M | M | M | c |
|Responsisbilty transfer to cloud Provider  | Physical DataCenter | M | M | M | c |

## Scenarios
Some common scenarios where PaaS might make sense include:

- Development framework: PaaS provides a framework that developers can build upon to develop or customize cloud-based applications. 
- Similar to the way you create an Excel macro, PaaS lets developers create applications using built-in software components. 
- Cloud features such as scalability, high-availability, and multi-tenant capability are included, reducing the amount of coding that developers must do.
- Analytics or business intelligence: Tools provided as a service with PaaS allow organizations to analyze and mine their data, finding insights and patterns and predicting outcomes to improve forecasting, product design decisions, investment returns, and other business decisions.




