@startuml
class Institution {
- name: String
- listStudents:List<Student>
- listStudents:List<Lecturer>
- listStudents:List<Course>
+ getName(): String
+ setListStudents():List<Student>
+ setListStudents():List<Lecturer>
+ setListStudents():List<Course>
}

class Lecturer {
- name: String
- listCourses: List<Course>
- listCourses: List<Student>
+ getName(): String
+ setListStudents():List<Course>
+ setListStudents():List<Student>
}

class Course {
- Name: String
- listCourses: List<Student>
- listCourses: List<Lecturer>
+ getName(): String
+ getListStudents():List<Student>
+ getListStudents():List<Lecturer>
}

class Student {
- name: String
- listCourses: List<Course>
- listLecturers: List<Lecturer>
+ getName(): String
+ getListCourses(): List<Course>
+ getListLecturer(): List<Lecturer>
}

Institution o-- Lecturer
Institution o-- Course
Institution o-- Student
Lecturer -- Course
Student --> Course
@enduml
