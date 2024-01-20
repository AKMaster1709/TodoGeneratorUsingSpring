# TodoGeneratorUsingSpring

# TodoGeneratorUsingSpring

# ToDo App using Spring Boot

Welcome to my ToDo app project! This simple application is built using the Spring Boot framework and allows users to manage their tasks efficiently.

## Project Overview

The ToDo app provides a user-friendly interface to create, update, and delete tasks. Users can also mark tasks as complete, helping them stay organized and on top of their responsibilities.
It also implements user authentication for personalized task list.

## Screenshots
![Web capture_20-1-2024_233220_localhost]((https://github.com/AKMaster1709/TodoGeneratorUsingSpring/blob/main/Web%20capture_20-1-2024_233220_localhost.jpeg))
![Web capture_20-1-2024_233251_localhost](https://github.com/AKMaster1709/TodoGeneratorUsingSpring/blob/main/Web%20capture_20-1-2024_233251_localhost.jpeg)
![Web capture_20-1-2024_233316_localhost](https://github.com/AKMaster1709/TodoGeneratorUsingSpring/blob/main/Web%20capture_20-1-2024_233316_localhost.jpeg)
![Web capture_20-1-2024_233344_localhost](https://github.com/AKMaster1709/TodoGeneratorUsingSpring/blob/main/Web%20capture_20-1-2024_233344_localhost.jpeg)


## Technologies Used

- Spring Boot
- Thymeleaf (or your chosen template engine)
- H2 Database
- Maven
- spring security

## Installation Instructions

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/todo-app.git
    ```

2. Navigate to the project directory:

    ```bash
    cd todo-app
    ```

3. Update the `application.properties` file with your MySQL database configuration:

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/todo
    spring.datasource.username=root
    spring.datasource.password=your-password
    ```

4. Build and run the application:

    ```bash
    mvn clean install
    java -jar target/todo-app-1.0.0.jar
    ```

5. Open your web browser and go to `http://localhost:8080` to start using the ToDo app.

## Project Structure

The project follows a standard Spring Boot structure:

- `src/main/java`: Contains the Java source code.
- `src/main/resources`: Contains configuration files, templates, and static resources.

## Code Samples

```java
@Controller
@SessionAttributes("name")
public class TodoControllerJpa {
	public TodoControllerJpa(TodoRepository todoRepository) {
		super();
		this.todoRepository = todoRepository;
	}
	private TodoRepository todoRepository;
	
	@RequestMapping("list-todos")
	public String listAllTodos(ModelMap model) {
		String username = getLoggedInUsername(model);
		List<Todo> todos = todoRepository.findByUsername(username);
		model.addAttribute("todos",todos);
		return "listTodos";
	}


    // ... other methods ...
}
```
## Contact Information
Feel free to reach out if you have any questions or feedback:

Email: abhishek.jain.aj1709@gmail.com
GitHub: https://github.com/AKMaster1709

## Acknowledgments
I want to express my gratitude to the Spring Boot community for providing excellent documentation and resources. 
