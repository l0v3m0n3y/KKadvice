# KKadvice
api for kk-advice.koyeb.app Kevin Kelly's Unsolicited Advice
# main
```cpp
#include "KKadvice.h"
#include <iostream>

int main() {
   KKadvice api;
    auto elections = api.get_random_advice().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    elections.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
