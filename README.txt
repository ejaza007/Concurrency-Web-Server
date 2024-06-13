Concurrent Web Server Project:


This project involves the development of a concurrent web server that manages HTTP requests using multiple threads, with the implementation of different scheduling policies to optimize the handling of these requests based on various criteria like file size and request order. This README outlines the server's architecture, features, and usage instructions.

Overview:

The web server is designed to handle multiple simultaneous connections efficiently by employing a thread pool and a scheduler that organizes requests based on a chosen scheduling policy. It supports both dynamic and static content, allowing it to serve web pages and execute server-side scripts.

Key Components:

Thread Pool: Manages a pool of worker threads that handle incoming requests concurrently.
Scheduler: Organizes incoming requests into a queue or a heap, depending on the scheduling policy, which can be FIFO (First In First Out), SFF (Smallest File First), or SFNF (Smallest File Name First).
Request Handler: Processes each request, serving both static files and dynamic content via CGI scripts.

Features:

Multiple Scheduling Policies:

FIFO: Handles requests in the order they arrive.
SFF: Prioritizes requests based on the size of the requested files, smallest first.
SFNF: Prioritizes requests based on the lexicographical order of file names.
Dynamic and Static Content Handling: The server can serve HTML pages, images, and execute CGI scripts, responding to both GET and POST requests.
Concurrent Request Handling: Utilizes a thread pool to manage and execute incoming requests in parallel, enhancing the server's ability to handle high loads.
Error Handling: Robust error handling to manage common HTTP errors like 404 Not Found, 400 Bad Request, and 403 Forbidden.


Compilation:

To compile the server, navigate to the server's directory and run:

1) make clean

2) make

3) ./wserver -d . -p 3000 -t 8 -b 16 -s FIFO/SFF/SFNF

4) Open a new terminal and run:

./wclient 127.0.0.1 3000 /test/1.html

To test the web server. Other test files may also be used