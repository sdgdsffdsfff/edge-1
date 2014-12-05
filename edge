#!/usr/bin/env python

"""
Edge - System Security Detection
@author  Feei(wufeifei@wufeifei.com)
@Version 0.1
@site    http://wufeifei.com/edge.html
"""

import re
import socket
import subprocess
import sys
import commands
import getopt
from datetime import datetime

class Edge:
    def __init__(self, argv):
        command = None
        usage = """
        edge 1.2 (http://wufeifei.com/edge.html)
        Uasge: edge [OPTION] [VALUE]

        -h      display this help and exit
        -v      output version and contact information and exit
        """
        version = """
        edge - System Security Detection
        Version : v1.2
        Author  : Feei
        Email:  : wufeifei@wufeifei.com
        Site:   : http://wufeifei.com/edge.html
        """
        try:
            opts, args = getopt.getopt(argv,"vhc:",["command="])
        except getopt.GetoptError:
            print 'ERROR:\'', ' '.join(argv), '\' NOT FOUND', "\n", usage
            sys.exit(2)
        for opt, arg in opts:
            if opt == '-h':
                print usage
                sys.exit()
            elif opt == '-v':
                print version
                sys.exit()
            elif opt in ('-c', '--command'):
                command = arg
            else:
                print usage
                
        if command == 'port':
            PortScan()
        elif command == 'login':
            system = SystemDetection()
            system.login_history()
        elif command == 'sysinfo':
            system = SystemDetection()
            system.information()
        else:
            print usage

class SystemDetection:
    loginHistory = []

    def __init__(self):
        print 'System Detection'

    def login_history(self):
        a, b = commands.getstatusoutput('last')
        if a == 0:
            self.loginHistory.append(b)
            arr = b.split("\n")
            del arr[len(arr) - 1]
            del arr[len(arr) - 1]
            for i in range(0, 20):
                line = '^-^'.join(arr[i].split())
                # 1NAME#2TTL#3IP#WEEK4#MONTH5#DAY6#STARTTIME7#-8#ENDTIME9#TOTALTIME10
                l = line.split('^-^')
                print l[0], l[2], l[4], '-' ,l[5] ,l[6] ,'-' ,l[8] , l[9]
    
    def information(self):
        a, b = commands.getstatusoutput('free -g')
        if a == 0:
            # MEM 0:TOTAL 1:USED 2:FREE 3:SHARE 4:BUFFERS 5:CACHED
            # SWAP 6:TOTAL 7:USED 8:FREE
            memory = re.findall('(\d+)', b)[0]
        a, b = commands.getstatusoutput('cat /etc/issue')
        if a == 0:
            system = b.split('\n')[0]
        a ,b = commands.getstatusoutput('df -h --total')
        if a == 0:
            # -4:SIZE -3:USED -2:AVAIL -1:USE%
            disk = re.findall('(\d+[G|%])', b)
        a ,b = commands.getstatusoutput('lscpu')
        if a == 0:
            cpucore = re.findall('CPU\(s\):\s+(\d+)\s+', b)[0]
            cpuid = re.findall('Vendor ID:\s+(\w+)\s+', b)[0]
            cpumhz = re.findall('CPU\ MHz:\s+(\d+).', b)[0]
        print 'System:', system
        print 'Memory:', memory
        print 'Disk:', disk[len(disk)-3], '/', disk[len(disk)-4], disk[len(disk)-1]
        print 'CPU:', cpuid, cpumhz, 'MHz', cpucore, 'Core'

class PortScan:
    remoteServerIP = None
    t1 = None
    t2 = None
    time = None
    ports = []

    def __init__(self):
        subprocess.call('clear', shell=True)
        Utility.echo('Scan Port')
        self.remoteServerIP = '127.0.0.1'
        self.t1 = datetime.now()
        self.scan()
        self.t2 = datetime.now()
        self.time = self.t2 - self.t1
        print "Scan Port Time:", self.time

    def scan(self):
        try:
            for port in range(1, 65535):
                sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
                result = sock.connect_ex((self.remoteServerIP, port))
                if result == 0:
                    self.ports.append(port)
                    print port, 'is OPEN'
                sock.close()

        except KeyboardInterrupt:
            print "Your can processed Ctrl+C"
            sys.exit()

        except socket.gaierror:
            print "Hostname couldn't be resolved.Exiting"
            sys.exit()

        except socket.error:
            print "Couldn't connect to server"
            sys.exit()

class WebsiteDetection:
    def __init__(self):
        pass

    def scan(website):
        pass

class Utility:
    def __init__(self):
        pass

    @staticmethod
    def echo(string):
        print '###############################################'
        print '#              ', string, '                    #'
        print '###############################################'

if __name__ == '__main__':
    Edge(sys.argv[1:])
