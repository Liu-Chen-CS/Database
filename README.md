# Database 

### Database Architecture
![MySQL drawio (1)](https://github.com/Liu-Chen-CS/Database/assets/158779475/07496cda-3923-45c2-bab8-258ec1701816)

### Storage Engine Layer
  - **Storage engines are `table-centric`:**
    - Each table can be associated with a specific storage engine during its creation.
    - The storage engine for an existing table can be modified using the `ALTER TABLE` command.
    - To get the SQL statement used to create the `table` example_table:
      - ![Snipaste_2024-03-08_10-55-54](https://github.com/Liu-Chen-CS/Database/assets/158779475/dd0a0488-91c3-470d-86d4-685ce68a3561)
    - To set up the `storage engine` for a table:
      - ![Snipaste_2024-03-08_11-12-47](https://github.com/Liu-Chen-CS/Database/assets/158779475/ef9b8036-3265-41f2-a391-01abb5f610f4)

  - **Index**
    - **What is it?**
      - Index is a `data structure` that improves the speed of data retrieval operations on a table by providing quick access to specific rows based on the values of one or more columns.
      - | Advantages    | Disadvantages |
        | -------- | ------- |
        | Retrieves data from a table efficiently   | Requires additional storage space on disk to store the index data structures |
        |                                           | Whenever data is inserted, updated, or deleted from the table, indexes need to be updated |
    - **Each storage engine has its own implementation of indexes:**
      - | Storage Engine    | Index |
        | -------- | ------- |
        | InnoDB|B+ Tree |
      - **B+ Tree**
        - Leaf nodes contain actual data records, leaf nodes are linked together to form a `linked list`.
       
    - **Index Management**
      - **How to create index** 
        -  <img width="226" alt="Screen Shot 2024-03-09 at 17 48 22" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/014e1f4b-9203-44b7-abc0-e5afdc16519d"><img width="317" alt="Screen Shot 2024-03-09 at 17 48 40" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/b27db6d4-27c7-4a05-8d86-554a09e248c4"><img width="317" alt="Screen Shot 2024-03-09 at 18 04 37" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/6e4e5fb1-1ff2-4e07-8797-4e51b59b37bf">

      - **How to check index**
        - <img width="237" alt="Screen Shot 2024-03-09 at 17 53 56" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/b6cd56fd-6d9c-4139-bc16-29bd823c7d55">
      - **How to delete index**
        - <img width="312" alt="Screen Shot 2024-03-09 at 17 54 43" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/aeebf088-683d-4093-b4df-fad99201cac4">
        
    - **Index Performance Optimization**
      - **SQL execution frequency**
        - The number of times a particular `SQL statement` is executed within a specific time period, enabling you to focus on optimizing those queries to improve overall performance.
        - <img width="322" alt="Screen Shot 2024-03-09 at 18 20 26" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/4e706279-e58a-431a-b0cf-f108f553b493">
        - <img width="373" alt="Screen Shot 2024-03-09 at 18 22 24" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/21914e5b-5de7-4d9e-9d3d-e741794f27b7">
        
      - **slow_query_log**
        - <img width="318" alt="Screen Shot 2024-03-09 at 18 29 43" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/3d89d9ed-80a4-4f6c-acb7-75c3e300196e"><img width="223" alt="Screen Shot 2024-03-09 at 18 31 38" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/949614b2-911b-4164-9f3c-08a3d976609c">
        - To enable the `slow_query_log`:
          - <img width="471" alt="Screen Shot 2024-03-09 at 18 44 18" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/de0bc32d-fb1a-4c0d-aaca-af37c3f64a80">
          - <img width="514" alt="Screen Shot 2024-03-09 at 18 44 51" src="https://github.com/Liu-Chen-CS/Database/assets/158779475/30556f2e-068c-421d-8c4e-81b9af3b434e">















