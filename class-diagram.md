
classDiagram
    class Main {
        -Scanner scanner
        -StudentService studentService
        +main(String[] args)
        -displayMenu()
        -addStudent()
        -listStudents()
        -searchStudent()
        -deleteStudent()
        -showSummary()
    }

    class StudentService {
        -List~Student~ students
        +addStudent(String name) boolean
        +getAllStudents() List~Student~
        +searchStudent(String name) Student
        +deleteStudent(String name) boolean
        +getStudentCount() int
    }

    class Student {
        -String name
        +Student(String name)
        +getName() String
        +setName(String name) void
        +toString() String
    }

    Main --> StudentService : uses
    StudentService "1" o-- "*" Student : manages
