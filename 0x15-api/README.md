Tasks
0. Gather data from an API
mandatory
Score: 0.0% (Checks completed: 0.0%)
Write a Python script that, using this REST API, for a given employee ID, returns information about his/her TODO list progress.

Requirements:

You must use urllib or requests module
The script must accept an integer as a parameter, which is the employee ID
The script must display on the standard output the employee TODO list progress in this exact format:
First line: Employee EMPLOYEE_NAME is done with tasks(NUMBER_OF_DONE_TASKS/TOTAL_NUMBER_OF_TASKS):
EMPLOYEE_NAME: name of the employee
NUMBER_OF_DONE_TASKS: number of completed tasks
TOTAL_NUMBER_OF_TASKS: total number of tasks, which is the sum of completed and non-completed tasks
Second and N next lines display the title of completed tasks: TASK_TITLE (with 1 tabulation and 1 space before the TASK_TITLE)
Example:

sylvain@ubuntu$ python3 0-gather_data_from_an_API.py 2
Employee Ervin Howell is done with tasks(8/20):
     distinctio vitae autem nihil ut molestias quo
     voluptas quo tenetur perspiciatis explicabo natus
     aliquam aut quasi
     veritatis pariatur delectus
     nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis
     repellendus veritatis molestias dicta incidunt
     excepturi deleniti adipisci voluptatem et neque optio illum ad
     totam atque quo nesciunt
sylvain@ubuntu$ python3 0-gather_data_from_an_API.py 4
Employee Patricia Lebsack is done with tasks(6/20):
     odit optio omnis qui sunt
     doloremque aut dolores quidem fuga qui nulla
     sint amet quia totam corporis qui exercitationem commodi
     sequi dolorem sed
     eum ipsa maxime ut
     tempore molestias dolores rerum sequi voluptates ipsum consequatur
sylvain@ubuntu$
sylvain@ubuntu$ python3 0-gather_data_from_an_API.py 4 | tr " " "S" | tr "\t" "T" 
EmployeeSPatriciaSLebsackSisSdoneSwithStasks(6/20):
TSoditSoptioSomnisSquiSsunt
TSdoloremqueSautSdoloresSquidemSfugaSquiSnulla
TSsintSametSquiaStotamScorporisSquiSexercitationemScommodi
TSsequiSdoloremSsed
TSeumSipsaSmaximeSut
TStemporeSmolestiasSdoloresSrerumSsequiSvoluptatesSipsumSconsequatur
sylvain@ubuntu$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x15-api
File: 0-gather_data_from_an_API.py
     
1. Export to CSV
mandatory
Score: 0.0% (Checks completed: 0.0%)
Using what you did in the task #0, extend your Python script to export data in the CSV format.

Requirements:

Records all tasks that are owned by this employee
Format must be: "USER_ID","USERNAME","TASK_COMPLETED_STATUS","TASK_TITLE"
File name must be: USER_ID.csv
Example:

sylvain@ubuntu$ python3 1-export_to_CSV.py 2
sylvain@ubuntu$ cat 2.csv
"2","Antonette","False","suscipit repellat esse quibusdam voluptatem incidunt"
"2","Antonette","True","distinctio vitae autem nihil ut molestias quo"
"2","Antonette","False","et itaque necessitatibus maxime molestiae qui quas velit"
"2","Antonette","False","adipisci non ad dicta qui amet quaerat doloribus ea"
"2","Antonette","True","voluptas quo tenetur perspiciatis explicabo natus"
"2","Antonette","True","aliquam aut quasi"
"2","Antonette","True","veritatis pariatur delectus"
"2","Antonette","False","nesciunt totam sit blanditiis sit"
"2","Antonette","False","laborum aut in quam"
"2","Antonette","True","nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis"
"2","Antonette","False","repudiandae totam in est sint facere fuga"
"2","Antonette","False","earum doloribus ea doloremque quis"
"2","Antonette","False","sint sit aut vero"
"2","Antonette","False","porro aut necessitatibus eaque distinctio"
"2","Antonette","True","repellendus veritatis molestias dicta incidunt"
"2","Antonette","True","excepturi deleniti adipisci voluptatem et neque optio illum ad"
"2","Antonette","False","sunt cum tempora"
"2","Antonette","False","totam quia non"
"2","Antonette","False","doloremque quibusdam asperiores libero corrupti illum qui omnis"
"2","Antonette","True","totam atque quo nesciunt"
sylvain@ubuntu$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x15-api
File: 1-export_to_CSV.py
     
2. Export to JSON
mandatory
Score: 0.0% (Checks completed: 0.0%)
Using what you did in the task #0, extend your Python script to export data in the JSON format.

Requirements:

Records all tasks that are owned by this employee
Format must be: { "USER_ID": [{"task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS, "username": "USERNAME"}, {"task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS, "username": "USERNAME"}, ... ]}
File name must be: USER_ID.json
Example:

sylvain@ubuntu$ python3 2-export_to_JSON.py 2
sylvain@ubuntu$ cat 2.json
{"2": [{"task": "suscipit repellat esse quibusdam voluptatem incidunt", "completed": false, "username": "Antonette"}, {"task": "distinctio vitae autem nihil ut molestias quo", "completed": true, "username": "Antonette"}, {"task": "et itaque necessitatibus maxime molestiae qui quas velit", "completed": false, "username": "Antonette"}, {"task": "adipisci non ad dicta qui amet quaerat doloribus ea", "completed": false, "username": "Antonette"}, {"task": "voluptas quo tenetur perspiciatis explicabo natus", "completed": true, "username": "Antonette"}, {"task": "aliquam aut quasi", "completed": true, "username": "Antonette"}, {"task": "veritatis pariatur delectus", "completed": true, "username": "Antonette"}, {"task": "nesciunt totam sit blanditiis sit", "completed": false, "username": "Antonette"}, {"task": "laborum aut in quam", "completed": false, "username": "Antonette"}, {"task": "nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis", "completed": true, "username": "Antonette"}, {"task": "repudiandae totam in est sint facere fuga", "completed": false, "username": "Antonette"}, {"task": "earum doloribus ea doloremque quis", "completed": false, "username": "Antonette"}, {"task": "sint sit aut vero", "completed": false, "username": "Antonette"}, {"task": "porro aut necessitatibus eaque distinctio", "completed": false, "username": "Antonette"}, {"task": "repellendus veritatis molestias dicta incidunt", "completed": true, "username": "Antonette"}, {"task": "excepturi deleniti adipisci voluptatem et neque optio illum ad", "completed": true, "username": "Antonette"}, {"task": "sunt cum tempora", "completed": false, "username": "Antonette"}, {"task": "totam quia non", "completed": false, "username": "Antonette"}, {"task": "doloremque quibusdam asperiores libero corrupti illum qui omnis", "completed": false, "username": "Antonette"}, {"task": "totam atque quo nesciunt", "completed": true, "username": "Antonette"}]}sylvain@ubuntu$
Repo:

GitHub repository: alx-system_engineering-devops
Directory: 0x15-api
File: 2-export_to_JSON.py
     
3. Dictionary of list of dictionaries
mandatory
Score: 0.0% (Checks completed: 0.0%)
Using what you did in the task #0, extend your Python script to export data in the JSON format.

Requirements:

Records all tasks from all employees
Format must be: { "USER_ID": [ {"username": "USERNAME", "task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS}, {"username": "USERNAME", "task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS}, ... ], "USER_ID": [ {"username": "USERNAME", "task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS}, {"username": "USERNAME", "task": "TASK_TITLE", "completed": TASK_COMPLETED_STATUS}, ... ]}
File name must be: todo_all_employees.json
Example:

sylvain@ubuntu$ python3 3-dictionary_of_list_of_dictionaries.py
sylvain@ubuntu$ cat todo_all_employees.json
{"1": [{"username": "Bret", "task": "delectus aut autem", "completed": false}, {"username": "Bret", "task": "quis ut nam facilis et officia qui", "completed": false}, {"username": "Bret", "task": "fugiat veniam minus", "completed": false}, {"username": "Bret", "task": "et porro tempora", "completed": true}, {"username": "Bret", "task": "laboriosam mollitia et enim quasi adipisci quia provident illum", "completed": false}, {"username": "Bret", "task": "qui ullam ratione quibusdam voluptatem quia omnis", "completed": false}, {"username": "Bret", "task": "illo expedita consequatur quia in", "completed": false}, {"username": "Bret", "task": "quo adipisci enim quam ut ab", "completed": true}, {"username": "Bret", "task": "molestiae perspiciatis ipsa", "completed": false}, {"username": "Bret", "task": "illo est ratione doloremque quia maiores aut", "completed": true}, {"username": "Bret", "task": "vero rerum temporibus dolor", "completed": true}, {"username": "Bret", "task": "ipsa repellendus fugit nisi", "completed": true}, {"username": "Bret", "task": "et doloremque nulla", "completed": false}, {"username": "Bret", "task": "repellendus sunt dolores architecto voluptatum", "completed": true}, {"username": "Bret", "task": "ab voluptatum amet voluptas", "completed": true}, {"username": "Bret", "task": "accusamus eos facilis sint et aut voluptatem", "completed": true}, {"username": "Bret", "task": "quo laboriosam deleniti aut qui", "completed": true}, {"username": "Bret", "task": "dolorum est consequatur ea mollitia in culpa", "completed": false}, {"username": "Bret", "task": "molestiae ipsa aut voluptatibus pariatur dolor nihil", "completed": true}, {"username": "Bret", "task": "ullam nobis libero sapiente ad optio sint", "completed": true}], "2": [{"username": "Antonette", "task": "suscipit repellat esse quibusdam voluptatem incidunt", "completed": false}, {"username": "Antonette", "task": "distinctio vitae autem nihil ut molestias quo", "completed": true}, {"username": "Antonette", "task": "et itaque necessitatibus maxime molestiae qui quas velit", "completed": false}, {"username": "Antonette", "task": "adipisci non ad dicta qui amet quaerat doloribus ea", "completed": false}, {"username": "Antonette", "task": "voluptas quo tenetur perspiciatis explicabo natus", "completed": true}, {"username": "Antonette", "task": "aliquam aut quasi", "completed": true}, {"username": "Antonette", "task": "veritatis pariatur delectus", "completed": true}, {"username": "Antonette", "task": "nesciunt totam sit blanditiis sit", "completed": false}, {"username": "Antonette", "task": "laborum aut in quam", "completed": false}, {"username": "Antonette", "task": "nemo perspiciatis repellat ut dolor libero commodi blanditiis omnis", "completed": true}, {"username": "Antonette", "task": "repudiandae totam in est sint facere fuga", "completed": false}, {"username": "Antonette", "task": "earum doloribus ea doloremque quis", "completed": false}, {"username": "Antonette", "task": "sint sit aut vero", "completed": false}, {"username": "Antonette", "task": "porro aut necessitatibus eaque distinctio", "completed": false}, {"username": "Antonette", "task": "repellendus veritatis molestias dicta incidunt", "completed": true}, {"username": "Antonette", "task": "excepturi deleniti adipisci voluptatem et neque optio illum ad", "completed": true}, {"username": "Antonette", "task": "sunt cum tempora", "completed": false}, {"username": "Antonette", "task": "totam quia non", "completed": false}, {"username": "Antonette", "task": "doloremque quibusdam asperiores libero corrupti illum qui omnis", "completed": false}, {"username": "Antonette", "task": "totam atque quo nesciunt", "completed": true}], "3": [{"username": "Samantha", "task": "aliquid amet impedit consequatur aspernatur placeat eaque fugiat suscipit", "completed": false}, {"username": "Samantha", "task": "rerum perferendis error quia ut eveniet", "completed": false}, {"username": "Samantha", "task": "tempore ut sint quis recusandae", "completed": true}, {"username": "Samantha", "task": "cum debitis quis accusamus doloremque ipsa natus sapiente omnis", "completed": true}, {"username": "Samantha", "task": "velit soluta adipisci molestias reiciendis harum", "completed": false}, {"username": "Samantha", "task": "vel voluptatem repellat nihil placeat corporis", "completed": false}, {"username": "Samantha", "task": "nam qui rerum fugiat accusamus", "completed": false}, {"username": "Samantha", "task": "sit reprehenderit omnis quia", "completed": false}, {"username": "Samantha", "task": "ut necessitatibus aut maiores debitis officia blanditiis velit et", "completed": false}, {"username": "Samantha", "task": "cupiditate necessitatibus ullam aut quis dolor voluptate", "completed": true}, {"username": "Samantha", "task": "distinctio exercitationem ab doloribus", "completed": false}, {"username": "Samantha", "task": "nesciunt dolorum quis recusandae ad pariatur ratione", "completed": false}, {"username": "Samantha", "task": "qui labore est occaecati recusandae aliquid quam", "completed": false}, {"username": "Samantha", "task": "quis et est ut voluptate quam dolor", "completed": true}, {"username": "Samantha", "task": "voluptatum omnis minima qui occaecati provident nulla voluptatem ratione", "completed": true}, {"username": "Samantha", "task": "deleniti ea temporibus enim", "completed": true}, {"username": "Samantha", "task": "pariatur et magnam ea doloribus similique voluptatem rerum quia", "completed": false}, {"username": "Samantha", "task": "est dicta totam qui explicabo doloribus qui dignissimos", "completed": false}, {"username": "Samantha", "task": "perspiciatis velit id laborum placeat iusto et aliquam odio", "completed": false}, {"username": "Samantha", "task": "et sequi qui architecto ut adipisci", "completed": true}], "4": [{"username": "Karianne", "task": "odit optio omnis qui sunt", "completed": true}, {"username": "Karianne", "task": "et placeat et tempore aspernatur sint numquam", "completed": false}, {"username": "Karianne", "task": "doloremque aut dolores quidem fuga qui nulla", "completed": true}, {"username": "Karianne", "task": "voluptas consequatur qui ut quia magnam nemo esse", "completed": false}, {"username": "Karianne", "task": "fugiat pariatur ratione ut asperiores necessitatibus magni", "completed": false}, {"username": "Karianne", "task": "rerum eum molestias autem voluptatum sit optio", "completed": false}, {"username": "Karianne", "task": "quia voluptatibus voluptatem quos similique maiores repellat", "completed": false}, {"username": "Karianne", "task": "aut id perspiciatis voluptatem iusto", "completed": false}, {"username": "Karianne", "task": "doloribus sint dolorum ab adipisci itaque dignissimos aliquam suscipit", "completed": false}, {"username": "Karianne", "task": "ut sequi accusantium et mollitia delectus sunt", "completed": false}, {"username": "Karianne", "task": "aut velit saepe ullam", "completed": false}, {"username": "Karianne", "task": "praesentium facilis facere quis harum voluptatibus voluptatem eum", "completed": false}, {"username": "Karianne", "task": "sint amet quia totam corporis qui exercitationem commodi", "completed": true}, {"username": "Karianne", "task": "expedita tempore nobis eveniet laborum maiores", "completed": false}, {"username": "Karianne", "task": "occaecati adipisci est possimus totam", "completed": false}, {"username": "Karianne", "task": "sequi dolorem sed", "completed": true}, {"username": "Karianne", "task": "maiores aut nesciunt delectus exercitationem vel assumenda eligendi at", "completed": false}, {"username": "Karianne", "task": "reiciendis est magnam amet nemo iste recusandae impedit quaerat", "completed": false}, {"username": "Karianne", "task": "eum ipsa maxime ut", "completed": true}, {"username": "Karianne", "task": "tempore molestias dolores rerum sequi voluptates ipsum consequatur", "completed": true}], "5": [{"username": "Kamren", "task": "suscipit qui totam", "completed": true}, {"username": "Kamren", "task": "voluptates eum voluptas et dicta", "completed": false}, {"username": "Kamren", "task": "quidem at rerum quis ex aut sit quam", "completed": true}, {"username": "Kamren", "task": "sunt veritatis ut voluptate", "completed": false}, {"username": "Kamren", "task": "et quia ad iste a", "completed": true}, {"username": "Kamren", "task": "incidunt ut saepe autem", "completed": true}, {"username": "Kamren", "task": "laudantium quae eligendi consequatur quia et vero autem", "completed": true}, {"username": "Kamren", "task": "vitae aut excepturi laboriosam sint aliquam et et accusantium", "completed": false}, {"username": "Kamren", "task": "sequi ut omnis et", "completed": true}, {"username": "Kamren", "task": "molestiae nisi accusantium tenetur dolorem et", "completed": true}, {"username": "Kamren", "task": "nulla quis consequatur saepe qui id expedita", "completed": true}, {"username": "Kamren", "task": "in omnis laboriosam", "completed": true}, {"username": "Kamren", "task": "odio iure consequatur molestiae quibusdam necessitatibus quia sint", "completed": true}, {"username": "Kamren", "task": "facilis modi saepe mollitia", "completed": false}, {"username": "Kamren", "task": "vel nihil et molestiae iusto assumenda nemo quo ut", "completed": true}, {"username": "Kamren", "task": "nobis suscipit ducimus enim asperiores voluptas", "completed": false}, {"username": "Kamren", "task": "dolorum laboriosam eos qui iure aliquam", "completed": false}, {"username": "Kamren", "task": "debitis accusantium ut quo facilis nihil quis sapiente necessitatibus", "completed": true}, {"username": "Kamren", "task": "neque voluptates ratione", "completed": false}, {"username": "Kamren", "task": "excepturi a et neque qui expedita vel voluptate", "completed": false}], "6": [{"username": "Leopoldo_Corkery", "task": "explicabo enim cumque porro aperiam occaecati minima", "completed": false}, {"username": "Leopoldo_Corkery", "task": "sed ab consequatur", "completed": false}, {"username": "Leopoldo_Corkery", "task": "non sunt delectus illo nulla tenetur enim omnis", "completed": false}, {"username": "Leopoldo_Corkery", "task": "excepturi non laudantium quo", "completed": false}, {"username": "Leopoldo_Corkery", "task": "totam quia dolorem et illum repellat voluptas optio", "completed": true}, {"username": "Leopoldo_Corkery", "task": "ad illo quis voluptatem temporibus", "completed": true}, {"username": "Leopoldo_Corkery", "task": "praesentium facilis omnis laudantium fugit ad iusto nihil nesciunt", "completed": false}, {"username": "Leopoldo_Corkery", "task": "a eos eaque nihil et exercitationem incidunt delectus", "completed": true}, {"username": "Leopoldo_Corkery", "task": "autem temporibus harum quisquam in culpa", "completed": true}, {"username": "Leopoldo_Corkery", "task": "aut aut ea corporis", "completed": true}, {"username": "Leopoldo_Corkery", "task": "magni accusantium labore et id quis provident", "completed": false}, {"username": "Leopoldo_Corkery", "task": "consectetur impedit quisquam qui deserunt non rerum consequuntur eius", "completed": false}, {"username": "Leopoldo_Corkery", "task": "quia atque aliquam sunt impedit voluptatum rerum as
