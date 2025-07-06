# Airflow Fundamentals Certification Preparation Questions

This document contains preparation questions for the Airflow Fundamentals Certification, covering key concepts, components, and configurations in Apache Airflow. Each question includes the correct answer(s) marked with a `+`.

## Question 1
**Which of the following are most likely the main requirements for running Airflow for production in a multi-team environment?** (Select all that apply)  
- [x] Multi-tenancy
- [x] Scalability
- [ ] Low cost
- [x] High availability

## Question 2
**Which of the following is the most likely way a solo developer will run Airflow for the purposes of experimentation and learning?**  
- [x] On a local machine or a free virtual machine (VM)
- [ ] On a paid cloud virtual machine (VM) service (e.g., EC2)
- [ ] On a multi-deployment cloud solution (e.g., EKS)
- [ ] On a highly secure on-premises architecture

## Question 3
**Which of the following are the most likely ways Airflow will be run in production by a single team?** (Select all that apply)  
- [x] On a container cloud offering (e.g., EKS)
- [x] On a fully-managed Airflow service (e.g., Astro)
- [x] On cloud virtual machines (e.g., EC2)
- [ ] On a single developer’s machine

## Question 4
**Which of the following is the most likely way a developer or team is going to run Airflow if they have to adhere to strict security or regulatory guidelines?**  
- [ ] On a cloud software
- [x] On-premise
- [ ] On a single developer’s machine

## Question 5
**Which of the following are most likely the main requirements for running Airflow for production as a single developer?** (Select all that apply)  
- [ ] High levels of scalability
- [x] Low infrastructure overhead
- [x] Low cost
- [ ] Multi-tenancy

## Question 6
**What is a task in Airflow?**  
- [ ] A configuration file for how Airflow is set up on a machine
- [ ] The entire data pipeline
- [ ] The direction the data pipeline executes
- [x] A single unit of work in a DAG

## Question 7
**Assume you are building a DAG and want to run a Python script. What type of Operator would you use to accomplish this goal?**  
- [ ] Sensor Operator
- [ ] Transfer Operator
- [x] Action Operator
- [ ] There are no Operators that allow a DAG to run a Python script

## Question 8
**Fill in the blank: In Airflow, an Operator is the specific work a _____ does.**  
- **Answer**: ______

## Question 9
**Assume you are building a DAG and want to move data from one system or data source to another. What type of Operator would you use to accomplish this goal?**  
- [x] Transfer Operator
- [ ] Sensor Operator
- [ ] There are no Operators that allow a DAG to move data from one system or data source to another
- [ ] Action Operator

## Question 10
**Assume you are building a DAG and want to wait for a file to load before executing the next task. What type of Operator would you use to accomplish this goal?**  
- [ ] Action Operator
- [ ] There are no Operators that allow a DAG to wait for something to load
- [x] Sensor Operator
- [ ] Transfer Operator

## Question 11
**Which of the following are characteristics of an Airflow DAG?** (Select all that apply)  
- [x] Graph based
- [ ] Represents multiple data pipelines
- [x] Composed of Tasks
- [ ] Cyclical
- [x] Directed

## Question 12
**Which of the following scenarios would be a valid use-case for Airflow?** (Select all that apply)  
- [x] Periodic analysis on sensor data from manufacturing equipment to forecast potential failures and schedule maintenance automatically +
- [ ] As a dedicated system for processing real-time, high-volume data streams for a stock trading application
- [x] A healthcare application that schedules email reminders for patients for their appointments
- [x] An AI chatbot that gives tips and solutions based on customer errors and actions

## Question 13
**The benefits of using a modern data orchestration tool like Airflow is because it offers the ability to...** (Select all that apply)  
- [x] Integrate with hundreds of external systems/software
- [x] Schedule data based on events in addition to time
- [ ] Author pipelines as configuration files
- [x] Use a rich feature set with features like built-in observability
- [ ] Store, secure, and preserve large quantities of data permanently

## Question 14
**Which of the following best describes the role of the scheduler in Airflow?**  
- [ ] To define connections to external systems (e.g., Data Warehouses)
- [ ] To store metadata about the state of tasks
- [ ] To execute the instructions defined in tasks
- [x] To determine which tasks need to be executed and when

## Question 15
**Which Airflow component is in charge of executing the logic of a DAG's tasks?**  
- [ ] The scheduler
- [x] The worker
- [ ] The metadata database
- [ ] The executor

## Question 16
**Which of the following best describes the role of an executor in Airflow?**  
- [x] To determine how and where tasks are executed
- [ ] To visualize the pipeline runs
- [ ] To execute the instructions of tasks
- [ ] To store tasks ready to be executed

## Question 17
**After creating your DAG in a Python file, which action do you need to take in order for Airflow to start the process of detecting and running your DAG?**  
- [ ] Launch the API server
- [ ] Restart Airflow and make sure the DAG is visible on the UI
- [ ] Wait for the DAG File Processor to pick up the tasks defined in the DAG
- [x] Put the Python file in the dags directory

## Question 18
**By default, how long can it take for the Airflow DAG File Processor to detect a new DAG file in the dags directory?**  
- [x] 5 minutes
- [ ] 1 minute
- [ ] 30 seconds
- [ ] 5 seconds

## Question 19
**Do the workers have direct access to the Airflow metadata database?**  
- [x] No
- [ ] Yes

## Question 20
**In which part of a DAG file would you specify how often you want to trigger the DAG?**  
- [ ] In the DAG's dependencies
- [ ] In the import statements
- [ ] In the DAG's tasks
- [x] In the DAG object definition

# Airflow Fundamentals Certification Preparation Questions (21-38)

## Question 21
**Assume a DAG has 3 tasks: task_extract, task_transform, and task_load. Which of the following represents the dependencies in a DAG that needs to meet the following conditions: task_transform is downstream of task_extract, task_load is downstream of task_transform?**  
- [ ] task_extract << task_load << task_transform
- [x] task_extract >> task_transform >> task_load
- [ ] task_extract >> task_load >> task_transform

## Question 22
**Which of the following Airflow components does the metadata database communicate with?**  
- [ ] The queue
- [x] The scheduler
- [x] The API server
- [x] The worker(s)

## Question 23
**What Astro CLI command will start running an Airflow project?**  
- **Answer**: `astro dev start`

## Question 24
**What is the purpose of the airflow_settings.yaml file in a new Airflow project generated by the Astro CLI?**  
- [ ] For storing Python files corresponding to data pipelines
- [ ] For specifying additional Python packages to install, along with their versions, to extend the functionality of the Airflow environment
- [x] For storing configurations such as connections and variables to prevent loss when recreating the local development environment
- [ ] For configuring Airflow instances via environment variables

## Question 25
**What Astro CLI command will generate a new Airflow project?**  
- **Answer**: `astro dev init`

## Question 26
**Which of the following are benefits of using the Astro CLI for local development?** (Select all that apply)  
- [ ] Its ability to dynamically generate new DAGs using AI
- [x] A variety of useful commands for managing an Airflow instance
- [x] Its ability to generate a standard project directory
- [x] To provide a streamlined experience for installing Airflow with limited prerequisites

## Question 27
**What is the purpose of the include directory in a new Airflow project generated by the Astro CLI?**  
- [ ] For storing configurations such as connections and variables to prevent loss when recreating the local development environment
- [ ] For configuring Airflow instances via environment variables
- [x] For storing files like SQL queries, bash scripts, or Python functions needed in data pipelines to keep them clean and organized
- [ ] For the customization of the Airflow instance by adding new operators or modifying the UI

## Question 28
**What's the best view to use to visualize your assets?**  
- [x] Asset View
- [ ] DAGs View
- [ ] Graph View

## Question 29
**What's the best view to check the historical states of the DAG Runs and Task Instances for a given DAG?**  
- [x] Grid View
- [ ] Graph View
- [ ] DAGs View

## Question 30
**What's the best view to get overall metrics of your Airflow instance?**  
- [x] The Home View
- [ ] Code View
- [ ] Asset View

## Question 31
**What's the best view to know if code updates have been applied?**  
- [ ] Home View
- [x] Code View
- [ ] Graph View

## Question 32
**What does the last column on the DAG View show?**  
- [x] DAG run states of current and previous DAG Runs for a given DAG
- [ ] Task's states of the current or latest DAG Run for a given DAG

## Question 33
**What's the role of the start date?**  
- [x] Define when the DAG starts being scheduled
- [ ] Define the trigger interval
- [ ] Avoid running past non-triggered DAG Runs

## Question 34
**What happens if you don't define a start date?**  
- [x] Nothing, it's optional
- [ ] That raises an error

## Question 35
**What's the role of tags?**  
- [x] They allow better organizing DAGs
- [x] They allow filtering DAGs
- [ ] They prevent from running DAGs that do not belong to the current user

## Question 36
**How can you avoid assigning the dag object to every task you create?**  
- [x] with DAG(...)
- [ ] dag = ...
- [x] @dag(...)
- [ ] You can't. You must assign the dag object to every task

## Question 37
**What happens when two DAGs share the same DAG id?**  
- [ ] The two DAGs appear on the UI
- [ ] You get an error
- [x] One DAG randomly shows up on the UI

## Question 38
**Does `task_a >> task_b >> task_c` is equivalent to `task_c << task_b << task_a`?**  
- [x] Yes
- [ ] No

## Question 39
**If a DAG runs every day at midnight with a `start_date=datetime(2025, 1, 1)`. When will the 3rd DAG run be triggered?**  
- [ ] 2025-01-01 00:00
- [ ] 2025-01-02 00:00
- [x] 2025-01-03 00:00
- [ ] 2025-01-04 00:00

## Question 40
**If a DAG with a "@daily" schedule is triggered at 00:00 on 2025-02-02. What's the logical date value for this DAG Run?**  
- [ ] 2025-02-01 00:00
- [x] 2025-02-02 00:00
- [ ] 2025-02-03 00:00

# Airflow Fundamentals Certification Preparation Questions (41-60)

## Question 41
**If a DAG with a "@daily" schedule is triggered at 00:00 on 2025-02-02. What's the `data_interval_end` value for this DAG Run (Assuming data intervals are used)?**  
- [ ] 2025-02-01
- [x] 2025-02-02
- [ ] 2025-02-03
- [ ] 2025-02-04

## Question 42
**With `catchup=False`, what happens when you run your DAG for the first time, and it has a `start_date` defined as 30 days ago?**  
- [ ] Nothing
- [x] The latest non-triggered DAG Run is triggered
- [ ] All non-triggered DAG Runs get triggered

## Question 43
**`logical_date = data_interval_start = data_interval_end` by default?**  
- [x] Yes
- [ ] No

## Question 44
**Select the 4 factors that define the uniqueness of an XCOM**  
- [x] key
- [x] value
- [ ] timestamp
- [x] dag_id
- [x] task_id
- [x] logical_date

## Question 45
**Is it possible to push an XCOM without explicitly specifying a key?**  
- [x] Yes
- [ ] No

## Question 46
**An XCOM is pushed into...**  
- [ ] The scheduler
- [ ] The worker
- [ ] The webserver
- [x] The database

## Question 47
**With Postgres, can you share 2Gb of data between 2 tasks with an XCOM?**  
- [ ] Yes
- [x] No

## Question 48
**How does the Scheduler know which XCOM to choose for a given DAG Run when multiple XCOMs have the same key, dag_id, and task_id?**  
- [ ] It selects one XCOM randomly
- [x] It selects the XCOM based on the logical date
- [ ] You can't have multiple XCOMs with the same key, dag_id, and task_id

## Question 49
**This DAG doesn’t show up on the UI. Why?**
```python
from airflow.decorators import dag,task
from pendulum import datetime
@dag(
    'test_dag',
    start_date = datetime(2023,3,1)
)
def test_dag():
    @task
    def test_task():
        return ' Hello World'
    test_task()
```
- [ ] The schedule parameter is missing
- [ ] The start_date is in the past
- [x] test_dag() is not called

## Question 50
**On manually triggering this DAG you don't see any task execution. Why?**
```python
from airflow.decorators import dag,task
from pendulum import datetime
@dag(
    'test_dag',
    start_date = datetime(3030,3,1)
)
def test_dag():
    @task
    def test_task():
        return 'Hello World'
    test_task()

test_dag()
```
- [ ] There is no end_date
- [x] The start_date is in the future
- [ ] Because there is only one task and no proper pipeline

## Question 51
**How many running DAG runs will you get as soon as you unpause this DAG?**
```python
from airflow.decorators import dag,task
from pendulum import datetime
@dag(
    'test_dag',
    start_date = datetime(2023,1,1),
    schedule = '@daily',
    catchup = False
)
def test_dag():
    @task
    def my_task():
        return 'Hello World'
    my_task()
test_dag()
```
- [ ] 0
- [x] 1
- [ ] 16
- [ ] 32

## Question 52
**You just finished writing your DAG and saved the file in the dags folder. How long will it take to appear on the UI?**  
- [x] By default it may take up to 5 minutes or more.
- [ ] It will be added instantly
- [ ] It may take up to 30 seconds.

## Question 53
**Is it possible to run tasks that are dependent on different versions of Python in the same DAG?**  
- [x] Yes
- [ ] No

## Question 54
**You can't find the connection type Amazon Web Services. What should you do?**  
- [x] Install the apache-airflow-providers-amazon
- [ ] Install boto3
- [ ] Use the http connection type

## Question 55
**If the file never arrives in the S3 bucket. When will the S3KeySensor time out?**  
- [ ] In 24 hours
- [x] In 7 days
- [ ] Never

## Question 56
**Does the Sensor instantly detect the file when it arrives in the bucket?**  
- [ ] Yes
- [x] No, it depends on the poke_interval

## Question 57
**Manually trigger the DAG `first_dag`, wait for having 3 tasks running then trigger the DAG `second_dag`. What's the task's state of `runme` in `second_dag`?**  
- [ ] running
- [ ] queued
- [x] scheduled

## Question 58
**How many worker slots are used?**  
- [x] 3
- [ ] 2
- [ ] 1

## Question 59
**Turn off the schedule of both DAGs and delete the two DAG runs by going to Browse and DAG Runs. Now, open the file `first_dag.py`, add a new parameter `mode='reschedule'` in `partial()`, save the file, and manually trigger `first_dag`. What is the status of the three tasks `waiting_for_files`?**  
- [ ] scheduled
- [ ] queued
- [ ] running
- [x] up_for_reschedule

## Question 60
**How many worker slots are running?**  
- [ ] 1
- [x] 0
- [ ] 3

# Airflow Fundamentals Certification Preparation Questions (61-79)

## Question 61
**Manually trigger the DAG `second_dag`. Does the task `runme` run?**  
- [x] Yes
- [ ] No

## Question 62
**Create a new empty file `data_1.csv` in the folder `include`. Go back to the Airflow UI and wait a minute. What do you see?**  
- [ ] Nothing
- [ ] 3 tasks are still up_for_reschedule
- [x] 1 sensor has been successfully executed

## Question 63
**A Sensor can be used for (Choose all that apply):**  
- [x] waiting for files to appear in an S3 bucket
- [x] waiting for a task in another DAG to complete
- [x] waiting for data to be present in a SQL table
- [x] waiting for a specified date and time

## Question 64
**You have a sensor that waits for a file to arrive in an S3 bucket. Your DAG runs every 10 mins, and it takes 8 mins to complete. What is the most appropriate timeout duration for the sensor? (in seconds)**  
- [ ] 60 * 60 * 24 * 7
- [ ] 60 * 60
- [x] 60 * 5

## Question 65
**What mode doesn't take a worker slot while a Sensor waits?**  
- [ ] poke
- [x] reschedule
- [ ] none

## Question 66
**What Sensor(s) can be used to apply logic conditions? (Choose all that apply)**  
- [x] PythonSensor
- [x] @task.sensor
- [ ] S3KeySensor

## Question 67
**What parameter can be useful to check for data to be present in a database without putting too much workload on each poke?**  
- [ ] timeout
- [x] exponential_backoff
- [ ] mode

## Question 68
**What is the purpose of `airflow db init` and when might you use it?**  
- [ ] Creates a new user in Airflow
- [ ] Generates a report of all DAGs currently in your Airflow environment
- [ ] Starts the Airflow web server
- [x] Initializes the Airflow metadata database, typically used when setting up Airflow for the first time

## Question 69
**What is the use case for `airflow config get-value` and how might you use it to troubleshoot issues?**  
- [ ] Lists all of the DAG files that have failed to import
- [x] Retrieves the value of a specific configuration option, useful for verifying that configuration settings are correctly set
- [ ] Verifies the validity of the Airflow metadata database schema
- [ ] Reserializes a DAG file to ensure that it can be properly loaded by Airflow

## Question 70
**You've recently upgraded your Airflow installation, but now your DAGs are not showing up in the UI. Which commands could you use to identify any import/parsing errors that might be preventing the DAG from being loaded?**  
- [x] airflow dags list-import-errors
- [ ] airflow dags show
- [x] airflow dags report
- [ ] airflow dags backfill

## Question 71
**Why would you use Airflow's backfill functionality?**  
- [ ] To test DAGs before deploying them to a production environment
- [ ] To reschedule a DAG to run at a different frequency
- [x] To fill in missing historical data that was not previously captured
- [ ] To remove all past DAG runs and start fresh with a new schedule

## Question 72
**What does the `airflow db check` command do?**  
- [ ] Upgrades the Airflow database schema to the latest version
- [x] Checks the connection to the Airflow database
- [ ] Removes all data from the Airflow database
- [ ] Initializes the Airflow database

## Question 73
**Can_you create two connections with identical IDs?**  
- [ ] Yes
- [x] No

## Question 74
**In Airflow, what is a connection?**  
- [ ] A connection is a way to define the order in which tasks in a DAG should be executed
- [ ] A connection is a type of sensor that waits for a specific condition to be met before proceeding with a task
- [x] A connection is a way to store and reuse credentials or configuration settings for external systems that are used in Airflow tasks

## Question 75
**What is the purpose of defining a connection in Airflow?**  
- [x] The purpose of defining a connection in Airflow is to avoid hard-coding sensitive information like passwords or API keys into Airflow DAGs, and to allow for easy management and reuse of connection information across multiple DAGs
- [ ] The purpose of defining a connection in Airflow is to store output data from tasks for later analysis
- [ ] The purpose of defining a connection in Airflow is to specify the order in which tasks should be executed within a DAG

## Question 76
**What are the different types of connections available in Airflow?**  
- [ ] Airflow only supports one type of connection, which is the SSH connection type
- [x] Airflow comes with several built-in connection types, including HTTP, MySQL, Postgres, SSH, and more. It also allows you to define custom connection types if needed
- [ ] Airflow supports a very limited set of connection types, including MongoDB, Cassandra, and Redis

## Question 77
**With 3 DAGs that fetch data from the same API. Does it make sense to store this API in a variable?**  
- [x] Yes
- [ ] No

## Question 78
**A variable can be stored in...**  
- [x] The metadata database
- [x] A secret backend
- [x] An environment variable
- [ ] The metaverse

## Question 79
**You create a variable with an environment variable. Does Airflow generate a connection to fetch the value of this variable?**  
- [ ] Yes
- [x] No