# Part 1. Python 

## Check installations
* **Make sure to have Jupyter Notebook installed**
  * If not: run `pip install notebook` in terminal

## Running the notebook
1. Download `TeikoTechTest.ipynb`
2. Open terminal and run `jupyter notebook' to start a jupyter server
3. On jupyter, find `TeikoTechTest.ipynb` in the Downloads folder (or in whichever directory you have downloaded it into)
4. Click `Run` --> `Run All Cells` 
   1. the `output.csv` will be generated as Number (1) requires
   2. The visualizations and significance results can all be seen on the notebook

<br>
<br>


# Part 2. Setting up the Database

## Installing PostgreSQL (and optionally pgAdmin)

* **PostgreSQL:** 
  * Here is the link to their official download page:  
    *  https://www.postgresql.org/download/
  * Once you install it, open the application
    * **Select `start`** 
      * **Ensure that it displays `"Running"` before proceeding or the script will not execute**
* **Optionally, install pgAdmin** 
  * This is a UI tool to conveniently view the schema
  * Here is the link to their official download page:
    * https://www.pgadmin.org/download/

## To Run the Script

1.  **Download the `create_db.sql` file from this repository.**

2.  **Navigate to the script in terminal**
    * Open a terminal and `cd` into the directory where you have downloaded `create_db.sql`
      * For example, say you download `create_db.sql` and this file is now in the `Downloads` folder, then starting from your home directory
        ```bash
        cd Downloads
        ```

3.  **Then run the script:**
    * Syntax

        ```bash
        psql -U <username> -f create_db.sql
        ```
        * Replace `<username>` with your username shown on the PostgreSQL app
          * If this doesn't work, try the default server `postgres` as your username
  
## Open pgAdmin to View Schema (Optional)

1.  On the left menu, right-click the `Databases` field and click `refresh`
2.  `cell_db` should now appear within `Databases`
3.  click `cell_db -> Schema -> Tables` and right-click the tables you want to observe, and select `View/edit Data` to see the layout
