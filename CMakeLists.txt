cmake_minimum_required(VERSION 3.26)
project(ConcurrentWebServer C)

set(CMAKE_C_STANDARD 11)

include_directories(.)

add_executable(ConcurrentWebServer
        circular_queue.c
        common_headers.h
        common_threads.h
        definitions.h
        heap.c
        helpers.c
        io_helper.c
        io_helper.h
        request.c
        request.h
        spin.c
        thread_pool.c
        thread_worker.c
        wclient.c
        wserver.c)
