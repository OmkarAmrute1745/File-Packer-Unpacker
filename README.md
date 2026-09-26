# File Packer Unpacker

A Java-based file packing and unpacking application developed to understand file handling, data processing, and GUI-based application development.

## Overview

The project provides a graphical interface for packing supported files into a single packed file and extracting files from a packed file.

The application includes:
- Login screen with username and password validation
- File packing through a Swing GUI
- File unpacking through a Swing GUI
- Support for `.txt`, `.c`, `.java`, and `.cpp` files
- Custom packed-file identification using the `Marvellous11` magic string
- File metadata stored in fixed-size headers
- Date, time, and day display in the GUI
- Navigation between login, pack, and unpack screens

## Project Structure

```text
File-Packer-Unpacker/
├── MarvellousMain.java
├── MarvellousPacker.java
├── MarvellousPackFront.java
├── MarvellousUnPack.java
├── MarvellousUnPackFront.java
├── NextPage.java
├── Template.java
├── README.md
└── .gitignore
```

## Technologies Used

- Java
- Java Swing
- Java AWT
- Java File I/O
- Java NIO
- Collections and Streams
- Multithreading

## How Packing Works

1. Start the application.
2. Log in using the configured credentials.
3. Select **Pack Files**.
4. Enter the source directory.
5. Enter the destination packed-file name.
6. The packer scans the directory recursively.
7. Files with supported extensions are added to the packed file.
8. Each file is stored with a fixed-size metadata header followed by its file data.

The packer writes the custom magic string `Marvellous11` at the beginning of the packed file. Supported extensions are defined in `MarvellousPacker.java`.

## How Unpacking Works

1. Select **Unpack Files**.
2. Provide the packed-file name.
3. The application reads and validates the `Marvellous11` magic string.
4. File metadata is read from each 100-byte header.
5. The stored file size is used to read the corresponding file data.
6. The extracted files are written back to the current location.

## Compile and Run

Compile all Java files:

```bash
javac *.java
```

Run the application:

```bash
java MarvellousMain
```

## Learning Outcomes

This project demonstrates practical concepts including:

- Java OOP
- Swing GUI development
- Event handling
- File and stream handling
- Directory traversal
- Java NIO
- Custom file formats
- Exception handling
- Basic multithreading
- GUI navigation

## Author

**Omkar Amrute**

Java Backend Developer | Java | Spring Boot
