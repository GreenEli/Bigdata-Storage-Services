# Bigdata-Storage-Services
## Engineering requirements:
Since the 21st century, information has entered an exponential explosive growth. The storage of massive big data has always been a hot spot for practical applications, and the security of information under big data conditions has always been the forefront of research, finally, massive big data should be highly efficient The characteristics of the query. The needs of this project are as follows:
1. Build a storage service platform that can store massive amounts of big data.
2. The storage service platform should be able to effectively guarantee data security.
3. The query of massive big data should be relatively fast and efficient.
## project instruction
1. After full consideration, the hbase cluster was finally elected as the storage database for massive big data, because it is built on the Hadoop ecosystem, it can make full use of the idle resources of the cluster for distributed computing and storage.
2. Provide effective security guarantee by constructing a special storage mode, open the project in IDEA, and the storage mode is as follows: this article designs four interrelated tables (user table, data table, permission token table, and association table), among which further improve the security performance of the tables created by users through the authority classification, that is, users can only have the right to own the tables they create, or the tokens owned by other creators can have the corresponding modification rights to other tables.
3. The query of the database uses the uniqueness of hbase's rowkey value on the one hand, and uses dictionary sorting to quickly query data, on the other hand, the storage structure of massive data is designed as a tree-like hierarchy (multiple tree structure) in this project, further optimization speeds up the efficiency of data query.
## Prepare the basics
1. The databases used in this project are MYSQL, HADOOP, HBASE.
2. The programming language of this project is java.
3. This project requires request testing of the network interface.
## Quick start instructions:
This project is carried out in a Linux environment based on the Ubuntu operating system, the programming tool used is IntelliJ IDEA, the network request testing tool used is insomnia, and the corresponding database version is MYSQL-5.6.47; hadoop-2.7.1; hbase -1.3.6.
### Quick start steps
1. After successfully installing the mysql, hadoop, and hbase databases, open the three databases in turn.

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/1.png)
 
2. Clone the code of this project to the local, and open the project in IDEA.

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/2.png)

3. Then copy the table building statement in hos-basic.sql, and execute the table building statement in the mysql terminal to create four interrelated tables.
 
![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/3.png)
 
4. Run the HosServerApp program to build a safe and efficient storage service platform for massive big data based on three databases, and open the test network port.

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/4.png)
 
5. Open the network test tool Insomnia, execute the insomnia_hos_api_test.json statement to initialize the test structure.

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/5.png)
 
6. Perform a normal test on the network test port.

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/6-1.png)

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/6-2.png)

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/6-3.png)

![image](https://github.com/GreenEli/Bigdata-Storage-Services/blob/main/pic1/6-4.png)
 
 
 
 
