nmon-cpu-analyse
================

Extract application's average CPU utilization from nmon log by
database (mysql) script.

How to get application's CPU utilization precisely and automatically?
---------------------------------------------------------------------

We often need an easy way to extract the CPU utilization of a software
after running a serial of testcases. For instance, we often run a
software with different configurations and analyse its performance
matrics including CPU utilization. This scenario repeats again and
again. The nmon-cpu-analyse is a SQL script to relief you from this
boring work.

How nmon-cpu-analyse works?
---------------------------

Generally, there are 4 steps.

1. start 'nmon' process to log system status.

2. start your testcase with startup time and finish time.

3. create database tables structure

4. manupulate nmon log to fit database tables

5. import munupulated nmon log into database

6. analyse CPU consumption with SQL script

nmon installation
-----------------

yum install -y ncurses ncurses-devel

wget http://sourceforge.net/projects/nmon/files/makefile/download
wget http://sourceforge.net/projects/nmon/files/lmon14i.c

mv lmon14i.c lmon.c

make nmon_x86_rhel52

root # mv nmon_x86_rhel52 /usr/local/bin/nmon

