# minii_project
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// Define structures
struct Patient {
    int id;
    char name[100];
    int age;
    char gender[10];
    // Add more fields as needed
};

struct Doctor {
    int id;
    char name[100];
    char specialization[100];
    // Add more fields as needed
};

struct Appointment {
    struct Patient patient;
    struct Doctor doctor;
    char date[20];
    char time[20];
    // Add more fields as needed
};

// Function to add a patient
void addPatient(struct Patient *patients, int *numPatients) {
    // Implementation
}

// Function to add a doctor
void addDoctor(struct Doctor *doctors, int *numDoctors) {
    // Implementation
}

// Function to schedule an appointment
void scheduleAppointment(struct Appointment *appointments, int *numAppointments,
                         struct Patient *patients, int numPatients,
                         struct Doctor *doctors, int numDoctors) {
    // Implementation
}

// Function to list appointments
void listAppointments(struct Appointment *appointments, int numAppointments) {
    // Implementation
}

int main() {
    struct Patient patients[100];
    struct Doctor doctors[20];
    struct Appointment appointments[500];
    int numPatients = 0;
    int numDoctors = 0;
    int numAppointments = 0;

    // Main loop for user interactions
    while (1) {
        // Display menu options and handle user input
        int choice;
        printf("Hospital Management System\n");
        printf("1. Add Patient\n");
        printf("2. Add Doctor\n");
        printf("3. Schedule Appointment\n");
        printf("4. List Appointments\n");
        printf("5. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addPatient(patients, &numPatients);
                break;
            case 2:
                addDoctor(doctors, &numDoctors);
                break;
            case 3:
                scheduleAppointment(appointments, &numAppointments, patients, numPatients, doctors, numDoctors);
                break;
            case 4:
                listAppointments(appointments, numAppointments);
                break;
            case 5:
                exit(0);
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }

    return 0;
}
