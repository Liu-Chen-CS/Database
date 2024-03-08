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



