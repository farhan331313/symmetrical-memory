# symmetrical-memory
"Symmetric memory system" refers to an architecture in which all memory modules are identical and interchangeable between multiple processors. In this context, each processor has equal access to 
class SymmetricalMemory:
    def __init__(self, size):
        self.memory = [0] * size  # Inisialisasi memori dengan ukuran tertentu
    
    def read(self, address):
        # Metode untuk membaca dari alamat memori tertentu
        return self.memory[address]
    
    def write(self, address, data):
        # Metode untuk menulis ke alamat memori tertentu
        self.memory[address] = data

# Contoh penggunaan:
if __name__ == "__main__":
    memory = SymmetricalMemory(1024)  # Inisialisasi objek memori dengan ukuran 1024
    
    # Prosesor 1 membaca dan menulis ke memori
    data1 = memory.read(0)
    memory.write(0, 10)
    
    # Prosesor 2 membaca dari alamat yang sama
    data2 = memory.read(0)
    
    # Output hasil
    print(f"Data yang dibaca oleh prosesor 1: {data1}")
    print(f"Data yang dibaca oleh prosesor 2: {data2}")
    
