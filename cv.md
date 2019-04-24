# Andrew Shavnev (Андрей Шавнёв)

## Contacts
_**phone:**_: +375336959382  
_**e-mail**_: andrevka@gmail.com

## Summary 
I like programming - it's interesting. I have more experience than the junior! 
Able to quickly understand unfamiliar code. 
I want to work in a large stable company, improving my skills and knowledge
     
## Skills 
* Confident knowledge in PHP (Yii2, Drupal), JavaScript (NodeJS), TypeScript (Angular), Python (Falcon, Nameko), Delphi, FoxPro, HTML, CSS
* Little experience using Java, Dart, Kotlin, C++ (QT), Perl, Bash
* Git
* Databases: 
    - SQL (MySql, Postgres, Firebird, MSSql, Sqlite)
    - NoSQL (MongoDB)
* ELK, Graphana, Sentry, Zipkin, Apache Zeppelin, Gitlab, RabbitMQ
* Linux (Debian, Ubuntu)
    
## Code samples

##### javascript

```javascript
/**
 * @param preferences - an array of integers. Indices of people, whom they love
 * @returns number of love triangles
 */
module.exports = function getLoveTrianglesCount(preferences = []) {
  let skp = [];
  let res = 0;

  for (i in preferences) {
    if (skp.indexOf(i * 1) > -1) {
      continue;
    }
    let first = [preferences[i], i * 1];
    let last = first;
    let s = [];

    for (j = 1; j < 4; j++) {

      if (last.join() == [preferences[last[0] - 1], last[0] - 1].join()) {
        last = [];
        break;
      }
      last = [preferences[last[0] - 1], last[0] - 1];
      s.push(last[0] - 1);
    }

    if (first.join() == last.join()) {
      res++;
      skp = skp.concat(s)
    }
  }
  return res;
};
```

##### python

```python
def run(self, task: BaseTask):
    """
    Метод для запуска всех заданий, наследованых от BaseTask
    :param task: проинициализированый объект задания
    :return:
    """
    try:
        return task.run()
    except Exception as ex:
        self.logger.error("ERROR",
                          class_name=task.__class__.__name__,
                          exception=ex.__class__.__name__,
                          description=str(ex),
                          task_uuid=task.uuid,
                          task_id=task.tid,
                          task=task.name,
                          exc_info=ex)
        data = {
            'debug': task.debugdata,
            'traceback':traceback.format_tb(ex.__traceback__)
        }
        self.bg_tasks.end_task(task.tid, status=-9, message="EXCEPTION ("+ex.__class__.__name__+"): "+str(ex), data=data)
        raise ex
```
    
## Experience
* _**2006-2008**_: FoxPro and Delphi developer
* _**2008-2013**_: Delphi developer, system administrator (Windows)
* _**2014-2019**_: Full stack developer in PU Vitebskoblgas (PHP, HTML, JS, TS, Databases)

At the moment I am working on a large project with microservice architecture. 
The project includes a mobile client, a web-based desktop application, a REST-full API in the backend, 
RPC microservices working through RabbitMQ

My first app on Angular. This is database of gas reduction units: 
* [Frontend](https://bitbucket.org/Andrew-6676/urg.angular2/src/master/) - angular 2, later upgraded to 5 
* [Backend](https://bitbucket.org/Andrew-6676/urg.yii2/src/master/) - PHP+Yii2

One of the first application on angular. It collects and displays temperature data from WellPro controllers using the Modbus protocol:
* [Backend (NodeJS+Express) + Frontend (Angular 2.4)](https://bitbucket.org/Andrew-6676/temperature/src/master/)
    
## Education
* _**2002-2006**_: Vitebsk polytechnical сollege - Software Support of Information Technologies  
* _**2006-2011**_: POLOTSKolotsk state university - faculty of information technologies - Software Support of Information Technologies
* _**2007**_: EPAM Java courses  
* _**2019**_: [Code Academy](https://www.codecademy.com/users/andrew1622305209/achievements) 
  
## English Skills
English Level: Pre-Intermediate  
Learning English started in school.   
