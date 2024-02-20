# Techsakshyam
This the Online Railway Reservation Service Project using Php


YouTube Link ::  https://youtu.be/1z723lVMNP8

A fully functional project based on Online Railway Reservation System Project which uses PHP Language with MySQL Database. The following PHP project contains all the essential features which can be in use by second-year IT students for their college projects. It has a number of features that will allow users to manage online ticket bookings. This web application’s concept is all clear. It’s the same as real-life scenarios and well-implemented on it. To download the free Online Railway Reservation System Project in PHP MySQL with source code files, please scroll down to the bottom of this post for the Download button

About Online Railway Reservation System PHP Project
In particular, this Railway Management System Project in PHP focuses mainly on managing online train tickets. To be more precise, the system helps to keep track of all online ticket bookings and information. Also, the system displays all the available passengers and routes. In addition, the system allows adding up train, and ticket details too(codeastro.com). Evidently, this project contains an admin panel with an employee and passenger panel. In an overview of this web application, passengers can simply register themselves and log into the system in order to book online tickets. He/she can view a list of available trains with their routes, fares, and others respectively. With it, passengers can book trains by selecting any. For this, the passenger has to check out the online train reservation by providing a payment code. At last, the passengers can view their tickets from the ticket section.

Before anything, this whole online ticket reservation process from a passenger’s account is not considered to be finalized by the system. Meaning, the tickets are set to pending status by default, which requires approval from the system administrator. From the ticket section, passenger can also print their tickets. Besides, the passengers can cancel their tickets anytime. Also, the users can view, and update their profiles.

Available Features:
Admin Panel
Passengers Panel
Employee Panel
Passengers Management
Train Management
Online Train Ticket Bookings
Cancel Ticket Bookings
View, Print Tickets
View, Update User Profiles
Search Available Trains
Employee Management
Manage Tickets
Approved, Pending Tickets
Accounting Overview

Admin Panel
An admin has full control over the system. He/she can manage passengers, trains, accounting, and so on. Here, each and every section has its own respective details such as name, and other important details. Here, an admin can add passenger records directly by filling up the required forms. During the passenger registration, an admin has to provide details such as name, address, contact, and set up login details. The administrator can also manage employee members for the system(codeastro.com). For adding an employee, the user has to provide names, and positions, and set up login credentials. Talking about the reservations, an administrator can view all the passenger’s reservation lists from his/her dashboard. Which also highlights all the important details such as names, routes, times, fares, total passengers, and more.

Train Management
When it comes to projects such as the Online Train Ticket Booking System, it’s a must that it should contain a section to cover train details too. And there is one. For this online train ticket system project, the administrator can manage train records easily. Not just with ease, but also it helps to cover up all the important and required information for the system. In order to add train details, the administrator has to provide a number of details. Such as the name of the train with the train number, route, fare, total seats/passengers, departure time, and more. Here, each and every train must have its own unique train number(codeastro.com). Besides, the administrator can view, update, and delete train details. And also, the system users can view and print the train details.

Train Ticket Management
Moreover, the tickets section is divided into three categories, Pending, Approved, and Management. As mentioned earlier, all the confirmed payments from the passenger’s ticket reservation are stored here for the admin’s approval. Here, the administrator can view a list of pending tickets with details such as the name of the passenger with his/her booking details. This particular section ties directly to the accounting section for the calculation of total ticket sales. After approval from the admin, the details are forwarded to the approved tickets section(codeastro.com). The admin can view payment codes from each and every passenger’s ticket reservations. In short, an admin has to mark and confirm the payment manually. Now talking about train ticket management, this section is where the administrator can either update the ticket details or delete the train ticket reservations


-- phpMyAdmin SQL Dump
-- version 4.6.5.2
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Dec 04, 2022 at 07:25 AM
-- Server version: 5.6.21
-- PHP Version: 5.6.3

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `orrsphp`
--

-- --------------------------------------------------------

--
-- Table structure for table `orrs_admin`
--

CREATE TABLE `orrs_admin` (
  `admin_id` int(20) NOT NULL,
  `admin_fname` varchar(200) NOT NULL,
  `admin_lname` varchar(200) NOT NULL,
  `admin_email` varchar(200) NOT NULL,
  `admin_uname` varchar(200) NOT NULL,
  `admin_pwd` varchar(200) NOT NULL,
  `admin_dpic` varchar(60) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_admin`
--

INSERT INTO `orrs_admin` (`admin_id`, `admin_fname`, `admin_lname`, `admin_email`, `admin_uname`, `admin_pwd`, `admin_dpic`) VALUES
(1, 'System ', 'Admin', 'vamshi@mail.com', 'Administrator', '903b21879b4a60fc9103c3334e4f6f62cf6c3a2d', 'admin-icn.png');

-- --------------------------------------------------------

--
-- Table structure for table `orrs_employee`
--

CREATE TABLE `orrs_employee` (
  `emp_id` int(20) NOT NULL,
  `emp_fname` varchar(200) NOT NULL,
  `emp_lname` varchar(200) NOT NULL,
  `emp_nat_idno` varchar(200) NOT NULL,
  `emp_phone` varchar(200) NOT NULL,
  `emp_addr` varchar(200) NOT NULL,
  `emp_uname` varchar(200) NOT NULL,
  `emp_email` varchar(200) NOT NULL,
  `emp_pwd` varchar(200) NOT NULL,
  `emp_dpic` varchar(200) NOT NULL,
  `emp_dept` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_employee`
--

INSERT INTO `orrs_employee` (`emp_id`, `emp_fname`, `emp_lname`, `emp_nat_idno`, `emp_phone`, `emp_addr`, `emp_uname`, `emp_email`, `emp_pwd`, `emp_dpic`, `emp_dept`) VALUES
(1, 'John', 'Deacon', '866861970', '+31024579651', '79 Green Avenue', 'deacon', 'employee@mail.com', '903b21879b4a60fc9103c3334e4f6f62cf6c3a2d', 'defaultimg.jpg', 'Train Captain');

-- --------------------------------------------------------

--
-- Table structure for table `orrs_passenger`
--

CREATE TABLE `orrs_passenger` (
  `pass_id` int(20) NOT NULL,
  `pass_fname` varchar(200) NOT NULL,
  `pass_lname` varchar(200) NOT NULL,
  `pass_phone` varchar(200) NOT NULL,
  `pass_addr` varchar(200) NOT NULL,
  `pass_email` varchar(200) NOT NULL,
  `pass_pwd` varchar(200) NOT NULL,
  `pass_dpic` varchar(200) NOT NULL,
  `pass_uname` varchar(200) NOT NULL,
  `pass_bday` varchar(200) NOT NULL,
  `pass_bio` longtext NOT NULL,
  `pass_train_number` varchar(200) NOT NULL,
  `pass_train_name` varchar(200) NOT NULL,
  `pass_dep_station` varchar(200) NOT NULL,
  `pass_dep_time` varchar(200) NOT NULL,
  `pass_arr_station` varchar(200) NOT NULL,
  `pass_train_fare` varchar(200) NOT NULL,
  `pass_fare_payment_code` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_passenger`
--

INSERT INTO `orrs_passenger` (`pass_id`, `pass_fname`, `pass_lname`, `pass_phone`, `pass_addr`, `pass_email`, `pass_pwd`, `pass_dpic`, `pass_uname`, `pass_bday`, `pass_bio`, `pass_train_number`, `pass_train_name`, `pass_dep_station`, `pass_dep_time`, `pass_arr_station`, `pass_train_fare`, `pass_fare_payment_code`) VALUES
(4, 'Christine', 'Moore', '7778885454', '44 Demo Address', 'christine@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'christine', '', '', 'CA556680', 'ZX Express', 'Test Station', '7:00 PM', 'Test Demo Station', '65', 'CAS0014587'),
(5, 'John', 'Barnes', '7412225698', '32 Ocello Street', 'johnk@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'johnbarnes', '', '', 'CA-777', 'Corridor Express', 'New York', '1:00 PM', 'Washington', '38', '102458700041'),
(6, 'Fritz', 'Mickk', '7412560000', '80 Russell Street', 'fritz@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'fritz', '', '', 'CA-007', 'Black Water', 'Chicago', '7:00 AM', 'Carbondale', '33', '107856452120'),
(7, 'Raisa', 'Taylor', '8542221450', '22 Valley Street', 'taylor@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'raisataylor', '', '', '', '', '', '', '', '', ''),
(8, 'Michael', 'Murdock', '7414587744', '43 Private Lane', 'murdock@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'murdock', '', '', '', '', '', '', '', '', ''),
(9, 'Greg', 'Alexander', '7458000015', '33 Pleasant Hill Road', 'greg@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'greg', '', '', '', '', '', '', '', '', ''),
(10, 'Dorothy', 'Garcia', '7458965555', '97 Euclid Avenue', 'garcia@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'dorothy', '', '', '', '', '', '', '', '', ''),
(11, 'Adele', 'Wilson', '7896547777', '28 Cook Hill Road', 'adelew@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'adele', '', '', '', '', '', '', '', '', ''),
(12, 'Martha', 'Meyer', '4570001569', '12 Eva Pearl Street', 'martha@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'martha', '', '', '', '', '', '', '', '', ''),
(13, 'Edna', 'Ashworth', '1475458500', '91 Timberbrook Lane', 'edna@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'edna', '', '', '', '', '', '', '', '', ''),
(14, 'Jody', 'Bennett', '7123650014', '60 Oral Lake Road', 'jody@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'jody', '', '', '', '', '', '', '', '', ''),
(15, 'Jerry', 'Campbell', '5478540000', '93 Sarah Drive', 'campbell@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'jerry', '', '', '', '', '', '', '', '', ''),
(16, 'Noelle', 'Ross', '3745698850', '41 Ray Court', 'ross@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'noelle', '', '', '', '', '', '', '', '', ''),
(17, 'William', 'Barnes', '6547778540', '31 Briarwood Road', 'wbarnes@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'wbarnes', '', '', '', '', '', '', '', '', ''),
(18, 'Fred', 'Jacquez', '6478540000', '17 Peck Court', 'fredj@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'fred', '', '', '', '', '', '', '', '', ''),
(19, 'Larry', 'Clark', '7696965450', '39 Dawson Drive', 'larry@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'larry', '', '', '', '', '', '', '', '', ''),
(20, 'Liam', 'Moore', '4750001458', '114 Southcross Avenue', 'liamoore@mail.com', '55c3b5386c486feb662a0785f340938f518d547f', 'defaultimg.jpg', 'liamoore', '', '', 'CA-778', 'Adirondack', 'Seattle', '6:00 AM', 'New York', '198', '100000789640');

-- --------------------------------------------------------

--
-- Table structure for table `orrs_passwordresets`
--

CREATE TABLE `orrs_passwordresets` (
  `pwd_id` int(20) NOT NULL,
  `email` varchar(200) NOT NULL,
  `status` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_passwordresets`
--

INSERT INTO `orrs_passwordresets` (`pwd_id`, `email`, `status`) VALUES
(1, 'employee@mail.com', 'Approved'),
(2, 'test21@mail.com', 'Pending');

-- --------------------------------------------------------

--
-- Table structure for table `orrs_train`
--

CREATE TABLE `orrs_train` (
  `id` int(20) NOT NULL,
  `name` varchar(200) NOT NULL,
  `route` varchar(200) NOT NULL,
  `current` varchar(200) NOT NULL,
  `destination` varchar(200) NOT NULL,
  `time` varchar(200) NOT NULL,
  `passengers` varchar(200) NOT NULL,
  `number` varchar(200) NOT NULL,
  `fare` varchar(2000) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_train`
--

INSERT INTO `orrs_train` (`id`, `name`, `route`, `current`, `destination`, `time`, `passengers`, `number`, `fare`) VALUES
(6, 'Black Water', 'Chicago - Carbondale', 'Chicago', 'Carbondale', '7:00 AM', '195', 'CA-007', '33'),
(10, 'ZX Express', 'Location One - Location Two', 'Test Station', 'Test Demo Station', '7:00 PM', '200', 'CA556680', '65'),
(11, 'Iron Range Express', 'Stockton - San Diego', 'Stockton', 'San Diego', '9:00 AM', '185', 'CA-697', '43'),
(12, 'Colonial', 'Boston - New York', 'Boston', 'New York', '10:45 AM', '255', 'CA-107', '35'),
(13, 'Corridor Express', 'New York - Washington', 'New York', 'Washington', '1:00 PM', '330', 'CA-777', '38'),
(14, 'Silver Meteor', 'New York - Miami', 'New York', 'Miami', '10:00 AM', '200', 'CA-707', '128'),
(15, 'Silver Star', 'New Orleans - Los Angeles', 'New Orleans', 'Los Angeles', '8:45 AM', '190', 'CA-107', '149'),
(16, 'Adirondack', 'Seattle - New York', 'Seattle', 'New York', '6:00 AM', '210', 'CA-778', '198'),
(17, 'Corridor Express', 'New York - Pittsfield', 'New York', 'Pittsfield', '12:45 PM', '195', 'CA-797', '45');

-- --------------------------------------------------------

--
-- Table structure for table `orrs_train_tickets`
--

CREATE TABLE `orrs_train_tickets` (
  `ticket_id` int(20) NOT NULL,
  `pass_name` varchar(200) NOT NULL,
  `pass_email` varchar(200) NOT NULL,
  `pass_addr` varchar(200) NOT NULL,
  `train_name` varchar(200) NOT NULL,
  `train_no` varchar(200) NOT NULL,
  `train_dep_stat` varchar(200) NOT NULL,
  `train_arr_stat` varchar(200) NOT NULL,
  `train_fare` varchar(200) NOT NULL,
  `fare_payment_code` varchar(200) NOT NULL,
  `confirmation` varchar(200) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `orrs_train_tickets`
--

INSERT INTO `orrs_train_tickets` (`ticket_id`, `pass_name`, `pass_email`, `pass_addr`, `train_name`, `train_no`, `train_dep_stat`, `train_arr_stat`, `train_fare`, `fare_payment_code`, `confirmation`) VALUES
(5, 'Christine Moore', 'christine@mail.com', '44 Demo Address', 'ZX Express', 'CA556680', 'Test Station', 'Test Demo Station', '65', 'CAS0014587', ''),
(6, 'John Barnes', 'johnk@mail.com', '32 Ocello Street', 'Iron Range Express', 'CA-697', 'Stockton', 'San Diego', '43', '102458700041', 'Approved'),
(7, 'John Barnes', 'johnk@mail.com', '32 Ocello Street', 'Corridor Express', 'CA-777', 'New York', 'Washington', '38', '102458700041', 'Approved'),
(8, 'Fritz Mickk', 'fritz@mail.com', '80 Russell Street', 'Black Water', 'CA-007', 'Chicago', 'Carbondale', '33', '107856452120', 'Approved'),
(9, 'Liam Moore', 'liamoore@mail.com', '114 Southcross Avenue', 'Adirondack', 'CA-778', 'Seattle', 'New York', '198', '100000789640', 'Approved');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `orrs_admin`
--
ALTER TABLE `orrs_admin`
  ADD PRIMARY KEY (`admin_id`);

--
-- Indexes for table `orrs_employee`
--
ALTER TABLE `orrs_employee`
  ADD PRIMARY KEY (`emp_id`);

--
-- Indexes for table `orrs_passenger`
--
ALTER TABLE `orrs_passenger`
  ADD PRIMARY KEY (`pass_id`);

--
-- Indexes for table `orrs_passwordresets`
--
ALTER TABLE `orrs_passwordresets`
  ADD PRIMARY KEY (`pwd_id`);

--
-- Indexes for table `orrs_train`
--
ALTER TABLE `orrs_train`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `orrs_train_tickets`
--
ALTER TABLE `orrs_train_tickets`
  ADD PRIMARY KEY (`ticket_id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `orrs_admin`
--
ALTER TABLE `orrs_admin`
  MODIFY `admin_id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;
--
-- AUTO_INCREMENT for table `orrs_employee`
--
ALTER TABLE `orrs_employee`
  MODIFY `emp_id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;
--
-- AUTO_INCREMENT for table `orrs_passenger`
--
ALTER TABLE `orrs_passenger`
  MODIFY `pass_id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=21;
--
-- AUTO_INCREMENT for table `orrs_passwordresets`
--
ALTER TABLE `orrs_passwordresets`
  MODIFY `pwd_id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;
--
-- AUTO_INCREMENT for table `orrs_train`
--
ALTER TABLE `orrs_train`
  MODIFY `id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=18;
--
-- AUTO_INCREMENT for table `orrs_train_tickets`
--
ALTER TABLE `orrs_train_tickets`
  MODIFY `ticket_id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=10;
/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;


**Recommended PHP Version: 5.6, 7.4, 8.1**


**Admin Login Details**

Email   : admin@mail.com
Password: codeastro.com
