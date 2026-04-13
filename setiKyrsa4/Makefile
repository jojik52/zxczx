# Компилятор и флаги
CXX = g++
CXXFLAGS = -std=c++11 -Wall -Wextra -g
LDFLAGS = -pthread

# Целевые файлы
TARGETS = server client

# Правила сборки
all: $(TARGETS)

server: server.cpp
	$(CXX) $(CXXFLAGS) -o server server.cpp $(LDFLAGS)
	@echo "✓ Server compiled successfully"

client: client.cpp
	$(CXX) $(CXXFLAGS) -o client client.cpp
	@echo "✓ Client compiled successfully"

# Очистка
clean:
	rm -f $(TARGETS)
	@echo "✓ Cleaned"

# Запуск сервера
run-server: server
	./server

# Запуск клиента
run-client: client
	./client

# Справка
help:
	@echo "Available targets:"
	@echo "  all         - Build all programs (default)"
	@echo "  server      - Build server only"
	@echo "  client      - Build client only"
	@echo "  clean       - Remove built programs"
	@echo "  run-server  - Run server"
	@echo "  run-client  - Run client"
	@echo "  help        - Show this help"

.PHONY: all clean run-server run-client help
