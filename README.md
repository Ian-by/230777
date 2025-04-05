# 230777
#include <stdio.h>
#include <unistd.h> // For sleep() function

// Function to simulate traffic light sequence using a for loop
void trafficLightForLoop(int cycles) {
    printf("Simulating traffic lights using FOR loop (%d cycles):\n", cycles);
    
    for (int i = 0; i < cycles; i++) {
        printf("\nCycle %d:\n", i + 1);
        
        // Red light
        printf("RED - Stop\n");
        sleep(3); // Wait for 3 seconds
        
        // Red + Yellow (prepare to go)
        printf("RED + YELLOW - Prepare to go\n");
        sleep(1);
        
        // Green light
        printf("GREEN - Go\n");
        sleep(4);
        
        // Yellow light (prepare to stop)
        printf("YELLOW - Prepare to stop\n");
        sleep(2);
    }
}

// Function to simulate traffic light sequence using a while loop
void trafficLightWhileLoop(int cycles) {
    printf("\nSimulating traffic lights using WHILE loop (%d cycles):\n", cycles);
    
    int count = 0;
    while (count < cycles) {
        printf("\nCycle %d:\n", count + 1);
        
        // Red light
        printf("RED - Stop\n");
        sleep(3);
        
        // Red + Yellow
        printf("RED + YELLOW - Prepare to go\n");
        sleep(1);
        
        // Green light
        printf("GREEN - Go\n");
        sleep(4);
        
        // Yellow light
        printf("YELLOW - Prepare to stop\n");
        sleep(2);
        
        count++;
    }
}

// Function to simulate traffic light sequence using a do-while loop
void trafficLightDoWhileLoop(int cycles) {
    printf("\nSimulating traffic lights using DO-WHILE loop (%d cycles):\n", cycles);
    
    int count = 0;
    do {
        printf("\nCycle %d:\n", count + 1);
        
        // Red light
        printf("RED - Stop\n");
        sleep(3);
        
        // Red + Yellow
        printf("RED + YELLOW - Prepare to go\n");
        sleep(1);
        
        // Green light
        printf("GREEN - Go\n");
        sleep(4);
        
        // Yellow light
        printf("YELLOW - Prepare to stop\n");
        sleep(2);
        
        count++;
    } while (count < cycles);
}

int main() {
    int cycles;
    
    printf("Traffic Lights Simulation Program\n");
    printf("Enter number of cycles to simulate: ");
    scanf("%d", &cycles);
    
    // Simulate using all three loop types
    trafficLightForLoop(cycles);
    trafficLightWhileLoop(cycles);
    trafficLightDoWhileLoop(cycles);
    
    printf("\nTraffic light simulation complete!\n");
    return 0;
}
