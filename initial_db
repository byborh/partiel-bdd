-- phpMyAdmin SQL Dump
-- version 5.1.2
-- https://www.phpmyadmin.net/
--
-- Host: localhost:8889
-- Generation Time: Mar 30, 2026 at 10:26 AM
-- Server version: 5.7.24
-- PHP Version: 8.1.0

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `snowboard`
--

-- --------------------------------------------------------

--
-- Table structure for table `athlete`
--

CREATE TABLE `athlete` (
  `id_athlete` int(11) NOT NULL,
  `nom` varchar(100) DEFAULT NULL,
  `prenom` varchar(100) DEFAULT NULL,
  `date_naissance` date DEFAULT NULL,
  `id_pays` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `athlete`
--

INSERT INTO `athlete` (`id_athlete`, `nom`, `prenom`, `date_naissance`, `id_pays`) VALUES
(1, 'Martin', 'Leo', '1998-05-10', 1),
(2, 'Dupont', 'Anna', '2000-07-21', 1),
(3, 'Smith', 'John', '1995-03-12', 2),
(4, 'Tanaka', 'Yuki', '1999-11-02', 4),
(5, 'Dubois', 'Claire', '1997-04-14', 1),
(6, 'Wilson', 'Emma', '1996-08-30', 2),
(7, 'Muller', 'Lukas', '1994-01-12', 5),
(8, 'Sato', 'Hana', '2001-06-18', 4),
(9, 'Garcia', 'Luis', '1997-09-10', 3),
(10, 'Rossi', 'Marco', '1996-02-14', 5),
(11, 'Kim', 'Min', '2000-12-01', 4);

-- --------------------------------------------------------

--
-- Table structure for table `critere`
--

CREATE TABLE `critere` (
  `id_critere` int(11) NOT NULL,
  `nom` varchar(100) DEFAULT NULL,
  `poids` decimal(5,2) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `critere`
--

INSERT INTO `critere` (`id_critere`, `nom`, `poids`) VALUES
(1, 'Technique', '3.00'),
(2, 'Amplitude', '2.00'),
(3, 'Style', '2.00'),
(4, 'Difficulte', '3.00');

-- --------------------------------------------------------

--
-- Table structure for table `editionjo`
--

CREATE TABLE `editionjo` (
  `id_edition` int(11) NOT NULL,
  `annee` int(11) NOT NULL,
  `ville` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `editionjo`
--

INSERT INTO `editionjo` (`id_edition`, `annee`, `ville`) VALUES
(1, 2026, 'Cortina');

-- --------------------------------------------------------

--
-- Table structure for table `epreuve`
--

CREATE TABLE `epreuve` (
  `id_epreuve` int(11) NOT NULL,
  `nom` varchar(100) NOT NULL,
  `date` date DEFAULT NULL,
  `id_edition` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `epreuve`
--

INSERT INTO `epreuve` (`id_epreuve`, `nom`, `date`, `id_edition`) VALUES
(1, 'Halfpipe', '2022-02-10', 1),
(2, 'Big Air', '2022-02-15', 1);

-- --------------------------------------------------------

--
-- Table structure for table `juge`
--

CREATE TABLE `juge` (
  `id_juge` int(11) NOT NULL,
  `nom` varchar(100) DEFAULT NULL,
  `id_pays` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `juge`
--

INSERT INTO `juge` (`id_juge`, `nom`, `id_pays`) VALUES
(1, 'Minnie M. Jones', 2),
(2, 'Hayley Borrie', 3),
(3, 'Tashimi Yamamoto', 4),
(4, 'Daniel M. Carr', 5),
(5, 'Claude L\'Hiver', 1),
(6, 'Michael R. Ladner', 2);

-- --------------------------------------------------------

--
-- Table structure for table `note`
--

CREATE TABLE `note` (
  `id_run` int(11) NOT NULL,
  `id_juge` int(11) NOT NULL,
  `id_critere` int(11) NOT NULL,
  `valeur` decimal(5,2) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `note`
--

INSERT INTO `note` (`id_run`, `id_juge`, `id_critere`, `valeur`) VALUES
(1, 1, 1, '85.00'),
(1, 1, 2, '80.00'),
(1, 1, 3, '78.00'),
(1, 1, 4, '82.00'),
(1, 2, 1, '88.00'),
(1, 2, 2, '85.00'),
(1, 2, 3, '84.00'),
(1, 2, 4, '86.00'),
(3, 1, 1, '70.00'),
(3, 1, 2, '75.00'),
(3, 1, 3, '72.00'),
(3, 1, 4, '74.00'),
(4, 2, 1, '90.00'),
(4, 2, 2, '88.00'),
(4, 2, 3, '91.00'),
(4, 2, 4, '89.00'),
(6, 1, 1, '82.00'),
(6, 1, 2, '80.00'),
(6, 1, 3, '79.00'),
(6, 1, 4, '81.00'),
(6, 2, 1, '84.00'),
(6, 2, 2, '83.00'),
(6, 2, 3, '82.00'),
(6, 2, 4, '85.00'),
(7, 2, 1, '88.00'),
(7, 2, 2, '86.00'),
(7, 2, 3, '87.00'),
(7, 2, 4, '89.00'),
(7, 3, 1, '85.00'),
(7, 3, 2, '84.00'),
(7, 3, 3, '83.00'),
(7, 3, 4, '86.00'),
(8, 1, 1, '78.00'),
(8, 1, 2, '76.00'),
(8, 1, 3, '75.00'),
(8, 1, 4, '77.00'),
(8, 3, 1, '80.00'),
(8, 3, 2, '79.00'),
(8, 3, 3, '78.00'),
(8, 3, 4, '81.00'),
(9, 1, 1, '90.00'),
(9, 1, 2, '88.00'),
(9, 1, 3, '89.00'),
(9, 1, 4, '91.00'),
(9, 2, 1, '87.00'),
(9, 2, 2, '86.00'),
(9, 2, 3, '88.00'),
(9, 2, 4, '89.00'),
(10, 2, 1, '83.00'),
(10, 2, 2, '82.00'),
(10, 2, 3, '81.00'),
(10, 2, 4, '84.00'),
(10, 3, 1, '85.00'),
(10, 3, 2, '84.00'),
(10, 3, 3, '83.00'),
(10, 3, 4, '86.00'),
(11, 1, 1, '86.00'),
(11, 1, 2, '85.00'),
(11, 1, 3, '84.00'),
(11, 1, 4, '87.00'),
(11, 2, 1, '88.00'),
(11, 2, 2, '87.00'),
(11, 2, 3, '86.00'),
(11, 2, 4, '89.00'),
(12, 2, 1, '90.00'),
(12, 2, 2, '88.00'),
(12, 2, 3, '89.00'),
(12, 2, 4, '91.00'),
(12, 3, 1, '87.00'),
(12, 3, 2, '86.00'),
(12, 3, 3, '88.00'),
(12, 3, 4, '89.00'),
(13, 1, 1, '82.00'),
(13, 1, 2, '81.00'),
(13, 1, 3, '80.00'),
(13, 1, 4, '83.00'),
(13, 3, 1, '84.00'),
(13, 3, 2, '83.00'),
(13, 3, 3, '82.00'),
(13, 3, 4, '85.00'),
(14, 1, 1, '85.00'),
(14, 1, 2, '84.00'),
(14, 1, 3, '83.00'),
(14, 1, 4, '86.00'),
(14, 2, 1, '87.00'),
(14, 2, 2, '86.00'),
(14, 2, 3, '85.00'),
(14, 2, 4, '88.00'),
(15, 1, 1, '91.00'),
(15, 1, 2, '90.00'),
(15, 1, 3, '89.00'),
(15, 1, 4, '92.00'),
(15, 2, 1, '88.00'),
(15, 2, 2, '87.00'),
(15, 2, 3, '86.00'),
(15, 2, 4, '89.00');

-- --------------------------------------------------------

--
-- Table structure for table `participation`
--

CREATE TABLE `participation` (
  `id_athlete` int(11) NOT NULL,
  `id_epreuve` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `participation`
--

INSERT INTO `participation` (`id_athlete`, `id_epreuve`) VALUES
(1, 1),
(2, 1),
(3, 1),
(4, 1),
(5, 1),
(6, 1),
(7, 1),
(8, 1),
(1, 2),
(3, 2),
(9, 2),
(10, 2),
(11, 2);

-- --------------------------------------------------------

--
-- Table structure for table `pays`
--

CREATE TABLE `pays` (
  `id_pays` int(11) NOT NULL,
  `nom` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `pays`
--

INSERT INTO `pays` (`id_pays`, `nom`) VALUES
(3, 'Canada'),
(1, 'France'),
(4, 'Japon'),
(5, 'Suisse'),
(2, 'USA');

-- --------------------------------------------------------

--
-- Table structure for table `run`
--

CREATE TABLE `run` (
  `id_run` int(11) NOT NULL,
  `id_athlete` int(11) DEFAULT NULL,
  `id_epreuve` int(11) DEFAULT NULL,
  `numero` int(11) DEFAULT NULL,
  `temps_execution` int(11) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Dumping data for table `run`
--

INSERT INTO `run` (`id_run`, `id_athlete`, `id_epreuve`, `numero`, `temps_execution`) VALUES
(1, 1, 1, 1, 45),
(2, 1, 1, 2, 48),
(3, 2, 1, 1, 44),
(4, 3, 1, 1, 47),
(5, 4, 1, 1, 46),
(6, 5, 1, 1, 46),
(7, 5, 1, 2, 49),
(8, 6, 1, 1, 45),
(9, 7, 1, 1, 48),
(10, 8, 1, 1, 47),
(11, 1, 2, 1, 50),
(12, 3, 2, 1, 52),
(13, 9, 2, 1, 51),
(14, 10, 2, 1, 49),
(15, 11, 2, 1, 48);

--
-- Indexes for dumped tables
--

--
-- Indexes for table `athlete`
--
ALTER TABLE `athlete`
  ADD PRIMARY KEY (`id_athlete`),
  ADD KEY `id_pays` (`id_pays`);

--
-- Indexes for table `critere`
--
ALTER TABLE `critere`
  ADD PRIMARY KEY (`id_critere`);

--
-- Indexes for table `editionjo`
--
ALTER TABLE `editionjo`
  ADD PRIMARY KEY (`id_edition`);

--
-- Indexes for table `epreuve`
--
ALTER TABLE `epreuve`
  ADD PRIMARY KEY (`id_epreuve`),
  ADD KEY `id_edition` (`id_edition`);

--
-- Indexes for table `juge`
--
ALTER TABLE `juge`
  ADD PRIMARY KEY (`id_juge`),
  ADD KEY `id_pays` (`id_pays`);

--
-- Indexes for table `note`
--
ALTER TABLE `note`
  ADD PRIMARY KEY (`id_run`,`id_juge`,`id_critere`),
  ADD KEY `id_juge` (`id_juge`),
  ADD KEY `id_critere` (`id_critere`);

--
-- Indexes for table `participation`
--
ALTER TABLE `participation`
  ADD PRIMARY KEY (`id_athlete`,`id_epreuve`),
  ADD KEY `id_epreuve` (`id_epreuve`);

--
-- Indexes for table `pays`
--
ALTER TABLE `pays`
  ADD PRIMARY KEY (`id_pays`),
  ADD UNIQUE KEY `nom` (`nom`);

--
-- Indexes for table `run`
--
ALTER TABLE `run`
  ADD PRIMARY KEY (`id_run`),
  ADD KEY `id_athlete` (`id_athlete`,`id_epreuve`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `athlete`
--
ALTER TABLE `athlete`
  MODIFY `id_athlete` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=12;

--
-- AUTO_INCREMENT for table `critere`
--
ALTER TABLE `critere`
  MODIFY `id_critere` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=5;

--
-- AUTO_INCREMENT for table `editionjo`
--
ALTER TABLE `editionjo`
  MODIFY `id_edition` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `epreuve`
--
ALTER TABLE `epreuve`
  MODIFY `id_epreuve` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=3;

--
-- AUTO_INCREMENT for table `juge`
--
ALTER TABLE `juge`
  MODIFY `id_juge` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;

--
-- AUTO_INCREMENT for table `pays`
--
ALTER TABLE `pays`
  MODIFY `id_pays` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;

--
-- AUTO_INCREMENT for table `run`
--
ALTER TABLE `run`
  MODIFY `id_run` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=16;

--
-- Constraints for dumped tables
--

--
-- Constraints for table `athlete`
--
ALTER TABLE `athlete`
  ADD CONSTRAINT `athlete_ibfk_1` FOREIGN KEY (`id_pays`) REFERENCES `pays` (`id_pays`);

--
-- Constraints for table `epreuve`
--
ALTER TABLE `epreuve`
  ADD CONSTRAINT `epreuve_ibfk_1` FOREIGN KEY (`id_edition`) REFERENCES `editionjo` (`id_edition`);

--
-- Constraints for table `juge`
--
ALTER TABLE `juge`
  ADD CONSTRAINT `juge_ibfk_1` FOREIGN KEY (`id_pays`) REFERENCES `pays` (`id_pays`);

--
-- Constraints for table `note`
--
ALTER TABLE `note`
  ADD CONSTRAINT `note_ibfk_1` FOREIGN KEY (`id_run`) REFERENCES `run` (`id_run`),
  ADD CONSTRAINT `note_ibfk_2` FOREIGN KEY (`id_juge`) REFERENCES `juge` (`id_juge`),
  ADD CONSTRAINT `note_ibfk_3` FOREIGN KEY (`id_critere`) REFERENCES `critere` (`id_critere`);

--
-- Constraints for table `participation`
--
ALTER TABLE `participation`
  ADD CONSTRAINT `participation_ibfk_1` FOREIGN KEY (`id_athlete`) REFERENCES `athlete` (`id_athlete`),
  ADD CONSTRAINT `participation_ibfk_2` FOREIGN KEY (`id_epreuve`) REFERENCES `epreuve` (`id_epreuve`);

--
-- Constraints for table `run`
--
ALTER TABLE `run`
  ADD CONSTRAINT `run_ibfk_1` FOREIGN KEY (`id_athlete`,`id_epreuve`) REFERENCES `participation` (`id_athlete`, `id_epreuve`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
