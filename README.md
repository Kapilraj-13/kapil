
CREATE DATABASE class_booking;

USE class_booking;

-- Table to store admin availability
CREATE TABLE availability (
    id INT AUTO_INCREMENT PRIMARY KEY,
    date DATE NOT NULL,
    start_time TIME NOT NULL,
    end_time TIME NOT NULL,
    available BOOLEAN DEFAULT TRUE
);

-- Table to store student bookings
CREATE TABLE bookings (
    id INT AUTO_INCREMENT PRIMARY KEY,
    student_name VARCHAR(100),
    student_email VARCHAR(100),
    booking_date DATE NOT NULL,
    start_time TIME NOT NULL,
    end_time TIME NOT NULL,
    status ENUM('pending', 'approved', 'cancelled') DEFAULT 'pending'
);
