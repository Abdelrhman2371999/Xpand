# **Student Management System & Cybersecurity Automation Project**

## **Project Overview**

This project combines C programming fundamentals with Python automation skills to create two integrated systems: 
1. A comprehensive **Student Management System in C** implementing data structures, algorithms, file handling, and user interfaces
2. A **Cybersecurity Automation Toolkit in Python** featuring network scanners, security utilities, and automation scripts

## **Project Architecture**

```
┌────────────────────────────────────────────────────────────────────┐
│                     DUAL-TECHNOLOGY PROJECT STACK                  │
│                                                                    │
│  ┌────────────────────────┐   ┌─────────────────────────────────┐  │
│  │    C PROGRAMMING       │   │      PYTHON AUTOMATION          │  │
│  │   Student Management   │   │    Cybersecurity Toolkit        │  │
│  │      System            │   │                                 │  │
│  │                        │   │                                 │  │
│  │ • Structures & Arrays  │   │ • Network Scanning & Monitoring │  │
│  │ • File Handling        │   │ • Security Automation           │  │
│  │ • Sorting & Searching  │   │ • Password Security Tools       │  │
│  │ • Pointers & Memory    │   │ • File Operations & Encryption  │  │
│  │ • Console UI           │   │ • System Integration            │  │
│  └────────────────────────┘   └─────────────────────────────────┘  │
│           ↑                               ↑                        │
│           └─────────────┬─────────────────┘                        │
│                         │                                          │
│                 ┌─────────────────┐                                │
│                 │   DATA FLOW     │                                │
│                 │   Integration   │                                │
│                 └─────────────────┘                                │
│                         ↑                                          │
│                 ┌─────────────────┐                                │
│                 │   FINAL OUTPUT  │                                │
│                 │  • C Application│                                │
│                 │  • Python Tools │                                │
│                 │  • Documentation│                                │
│                 └─────────────────┘                                │
└────────────────────────────────────────────────────────────────────┘
```

### **System Specifications**

#### **C Programming Component**
- **Language**: Pure C (ANSI C/C99)
- **Application**: Console-based Student Management System
- **Core Features**: Structures, Arrays, File I/O, Algorithms
- **Output**: Executable application with menu system

#### **Python Component**
- **Language**: Python 3.x
- **Application**: Cybersecurity Automation Toolkit
- **Core Features**: Network scanning, File operations, Security utilities
- **Output**: Python scripts and automation tools

## **Part 1: C Programming - Student Management System**

### **Project Requirements**

#### **1.1 Structure Definition**
Define a `Student` structure with:
- Student ID (integer)
- Full Name (character array, 50 characters)
- Age (integer)
- Total Marks (float)
- Average (float)
- Grade (character)

#### **1.2 Data Management**
- Create array of `Student` structures for 5 students
- Implement input functions with validation:
  - Age: 17-25
  - Marks: 0-400
- Display records in formatted table

#### **1.3 Core Functions**
1. `calculateAverage()` - Individual student average (Marks/4)
2. `calculateClassAverage()` - Overall class average
3. `assignGrade()` - Letter grades (A-F scale)
4. `searchStudent()` - Linear search by ID
5. `sortStudents()` - Bubble sort by Total Marks (descending)

#### **1.4 Advanced Features**
- Pointer-based array traversal
- File handling (save/load to "students.txt")
- Menu-driven interface
- Update student records function

### **Implementation Checklist - C Component**
- [ ] Structure definition and array declaration
- [ ] Input validation with do-while loops
- [ ] All required functions implemented
- [ ] Linear search algorithm working
- [ ] Bubble sort algorithm working
- [ ] File save/load operations
- [ ] Menu system with all options
- [ ] Pointer usage demonstrated
- [ ] Code documentation and comments

## **Part 2: Python - Cybersecurity Automation Toolkit**

### **Project Requirements**

#### **2.1 Security Utilities**
1. **Password Strength Checker**
   - Validate password criteria
   - Use regular expressions (re library)
   - Criteria: 8+ chars, upper/lowercase, digit, special char

2. **Network Scanner**
   - IP address scanner
   - Port scanner for specific ranges
   - Integration with socket library

#### **2.2 File Operations**
1. **File and Directory Management**
   - Create files and directories programmatically
   - File content manipulation
   - OS integration

2. **Basic Encryption Tool**
   - File encryption demonstration
   - Use cryptography library
   - Secure file operations

#### **2.3 System Automation**
1. **Web Automation**
   - Open URLs programmatically
   - Basic browser integration

2. **System Monitoring Tools**
   - Process monitoring
   - System information gathering

### **Implementation Checklist - Python Component**
- [ ] Password strength checker with regex
- [ ] IP scanner using ping commands
- [ ] Port scanner with socket library
- [ ] File creation and management scripts
- [ ] Directory operations
- [ ] Basic encryption demonstration
- [ ] Web automation script
- [ ] Error handling with try-except blocks
- [ ] Function-based modular design

## **Project Timeline (1 Week)**

### **Day 1-2: Planning & Setup**
- Review project requirements
- Set up development environment
- Create project structure
- Plan data flow between components

### **Day 3-4: Core Implementation**
- **Morning**: C Structure and basic functions
- **Afternoon**: Python security utilities
- **Evening**: Integration planning

### **Day 5-6: Advanced Features**
- **Morning**: C File handling and pointers
- **Afternoon**: Python automation scripts
- **Evening**: Testing and debugging

### **Day 7: Integration & Documentation**
- Final testing of both components
- Create comprehensive documentation
- Prepare demonstration
- Final submission preparation

## **Software Requirements Specification (SRS)**

### **1. Functional Requirements**

#### **C System Requirements:**
1. **Data Input**
   - Accept student data with validation
   - Handle invalid input with re-prompt
   - Store data in structured format

2. **Data Processing**
   - Calculate individual and class statistics
   - Implement searching and sorting algorithms
   - Generate grades based on marks

3. **Data Persistence**
   - Save data to text file
   - Load data from text file
   - Maintain data integrity

4. **User Interface**
   - Console-based menu system
   - Formatted data display
   - User-friendly prompts

#### **Python System Requirements:**
1. **Security Tools**
   - Password validation with multiple criteria
   - Network connectivity testing
   - Port availability checking

2. **File Operations**
   - Create and manipulate files
   - Directory management
   - Basic file encryption

3. **Automation**
   - System command execution
   - Web browser control
   - Process management

### **2. Non-Functional Requirements**

#### **Performance:**
- C application: Response time < 2 seconds for all operations
- Python scripts: Efficient execution for network scanning
- Memory efficient data structures

#### **Usability:**
- Intuitive menu systems
- Clear error messages
- Comprehensive help/instructions

#### **Reliability:**
- Data validation on all inputs
- Error handling for file operations
- Graceful failure handling

#### **Portability:**
- Platform-independent C code
- Cross-platform Python scripts
- Standard library usage

### **3. Technical Constraints**
- Pure C (no C++ features)
- Python 3.x standard libraries
- Console-based interface only
- No database systems (file-based storage only)

## **Deliverables**

### **1. C Programming Deliverables**
- Complete Student Management System source code
- Executable application
- Sample data files
- User manual/documentation

### **2. Python Deliverables**
- Cybersecurity toolkit scripts
- Password checker utility
- Network scanner tools
- File operation scripts
- Documentation for each tool

### **3. Combined Deliverables**
- Project report documenting:
  - Implementation approach
  - Challenges faced
  - Solutions implemented
  - Testing results
- Demonstration video (optional but recommended)
- Source code with comprehensive comments

## **Grading Rubric**

| **Category** | **C Points** | **Python Points** | **Total** |
|-------------|--------------|-------------------|-----------|
| **Code Quality** | 15 | 10 | 25 |
| **Functionality** | 20 | 15 | 35 |
| **Algorithm Implementation** | 10 | 5 | 15 |
| **Error Handling** | 5 | 5 | 10 |
| **Documentation** | 5 | 5 | 10 |
| **Innovation/Extra Features** | 5 | 0 | 5 |
| **Total** | **60** | **40** | **100** |

## **Submission Guidelines**

### **File Structure:**
```
project/
├── C_Component/
│   ├── main.c
│   ├── student.h
│   ├── student.c
│   ├── file_ops.c
│   └── Makefile
├── Python_Component/
│   ├── password_checker.py
│   ├── network_scanner.py
│   ├── file_manager.py
│   └── automation_tools.py
├── Documentation/
│   ├── Project_Report.pdf
│   ├── User_Manual.md
│   └── Test_Cases.txt
└── README.md
```

### **Submission Format:**
- Compressed archive (ZIP format)
- Include all source files
- Include sample data files
- Include documentation
- Submission deadline: 1 week from assignment date

## **Important Notes**

1. **Academic Integrity**: All code must be your original work
2. **Code Comments**: Comprehensive comments explaining logic
3. **Testing**: Include test cases and validation
4. **Backup**: Regular backup of your work
5. **Questions**: Ask for clarification early if needed

## **Success Criteria**

- C application compiles without errors/warnings
- All menu options function correctly
- Python scripts execute without errors
- File operations work correctly
- Algorithms produce correct results
- User interface is intuitive
- Documentation is comprehensive

## **Getting Help**

- Review provided presentation materials
- Consult C and Python reference documentation
- Test incrementally as you develop
- Seek clarification for ambiguous requirements
- Use debugging tools effectively

---
