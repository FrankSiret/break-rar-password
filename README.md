# Break into rar file

This project was for personal reasons, I forgot one of my passwords from a rar file, so I created a way to break it using keywords that I commonly used as I recall.

In the `void MainWindow::on_start()` [function](./mainwindow.cpp?line=27), notice that there is a variable named `dic` which is basically a list of string vectors `QVector<QVector<QString>> dic`, this is filled with some fake patterns for testing purposes only and right after that the `generatePassword()` method, which starts the execution of the algorithm in a threaded process.

### How it is work?

In the order that all `dic` vectors are arranged, the algorithm concatenates all possible combinations and tests them in the rar file using the protocol available for rar files `unrar x -p<password> <soruce> <sink>`

### Somthink you should know

* The algorithm is based on known password patterns.
* Is not designed to force passwords of all kind of rar.
* **And you must use it under your own consent.**

### Technologies

`C++` 
`Qt 6`

### Licence 

MIT