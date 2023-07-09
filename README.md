# airflow
https://pplearn.udemy.com/course/the-complete-hands-on-course-to-master-apache-airflow/learn/lecture/32787474#overview

<br><br><br>

# Get started with airflow
## 1. What is airflow?
an open source platform to programmatically author, schedule and monitor workflows

<br><br><br>

## 2. Core components
1. Web server
2. Scheduler
3. Metastore
4. Trigger
5. Executor
6. Queue
7. Worker
- ![imgs](./imgs/Xnip2023-07-09_10-58-12.jpg)


## 3. Core concepts

1. DAG (Directed Acyclic Graph)
    - ![imgs](./imgs/Xnip2023-07-09_11-00-26.jpg)


2. Operator
    - Action Opeartor
    - Transfer Operators
    - Sensor Operators
    - ![imgs](./imgs/Xnip2023-07-09_11-01-39.jpg)
    


3. Task/ Task Instance
    - ![imgs](./imgs/Xnip2023-07-09_11-02-54.jpg)

4. Workflow
    - ![imgs](./imgs/Xnip2023-07-09_11-03-14.jpg)

<br><br><br>

## 4. Airflow is not
Airflow is not a `data streaming` solution neither a `data processing` framework

<br><br><br>

## 5. Single node architectures

![imgs](./imgs/Xnip2023-07-09_11-09-01.jpg)

<br><br><br>

## 6. Multi Nodes architecture (Celery)
![imgs](./imgs/Xnip2023-07-09_11-11-55.jpg)



## 7. Execution flow

1. create a new dag.py and put into folder of `dags`
    - ![imgs](./imgs/Xnip2023-07-09_11-20-15.jpg)

2. every 5 minute detect new dag/ 30s after modification
    - ![imgs](./imgs/Xnip2023-07-09_11-20-05.jpg)

3. Scheduler runs dag and create DagRun Object with state `running`
    - ![imgs](./imgs/Xnip2023-07-09_11-19-50.jpg)

4. schedules taskinstance object state `null` and scheduled
    - ![imgs](./imgs/Xnip2023-07-09_11-19-39.jpg)
5. sends taskintance to the Executor, taskinstance `queued`
    - ![imgs](./imgs/Xnip2023-07-09_11-19-27.jpg)
6. Executor create sub process to run the task
    - ![imgs](./imgs/Xnip2023-07-09_11-19-16.jpg)
7. taskinstance in `running` state
    - ![imgs](./imgs/Xnip2023-07-09_11-19-06.jpg)
8. and taskinstance is in success or failed
    - ![imgs](./imgs/Xnip2023-07-09_11-18-41.jpg)

<br><br><br>

## 8. installing apache airflow
- (startup airflow)[https://airflow.apache.org/docs/apache-airflow/2.5.1/docker-compose.yaml]
```bash
$ docker-compose up -d

$ docker-compose ps

```
- ![imgs](./imgs/Xnip2023-07-09_11-36-21.jpg)

<br><br><br>

## 9. docker compose
