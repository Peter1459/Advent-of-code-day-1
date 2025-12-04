# Advent-of-code-day-1

f = open("ac1.txt")

count = 0
pos = 50 #50
num = 0

for line in range(4776): #4776
    l = f.readline()
    l = l.strip()
    if l[0] == 'L':
        num = int(l[1:])
        for i in range(num):
            pos -= 1
            if pos == 100:
                pos = 0
            if pos == -1:
                pos = 99
            if pos == 0:
                count += 1
    elif l[0] == 'R':
        num = int(l[1:])
        for i in range(num):
            pos += 1
            if pos == 100:
                pos = 0
            if pos == -1:
                pos = 99
            if pos == 0:
                count += 1

print(count, "count")
