'''
Podatke iz datoteke rezultati.csv učitati kao listu ntorki oblika
ime, prezime, bodovi).
Iterirati kroz sve studente i ispisati samo one koji su položili ispit
br. bodova veci od 49)

Iz podataka učitanih u prethodnom primjeru sortirati listu po prezimenima.
Napraviti novi rječnik gdje će se po bodovnom rangu upisivati broj
ostvarenih ocjena. 

Nedovoljan
0-49%

Dovoljan
50-65%

Dobar
65-80%

Vrlodobar
80-90%

Izvrstan
90-100%
'''

import csv

with open('studenti.csv', mode='r', encoding='utf-8') as file:
    csv_reader = csv.reader(file)
    rows = list(csv_reader)
    if len(rows) >= 3:
        rows = rows[4:-3]
    list_of_tuples = list(map(tuple, rows))


studenti = []
for n in list_of_tuples:
    student = (n[:-2])
    studenti.append(student)

print(studenti)
    
def polozili(studenti):
    polozili = []
    for i  in studenti:
        bodovi = i[2]
        if int(bodovi)>45:
            polozili.append(i)
    return polozili

print(f"\nPoložili su: \n {polozili(studenti)}")

def sortiranje(studenti):
    return studenti[1]

sortirani = sorted(studenti, key=sortiranje)
print(f"\nStudenti sortirani po prezimenima: \n {sortirani}")

for student in sortirani:
    bodovi = int(student[2])
    if bodovi <100 and bodovi >= 90:
        print(f"\nStudent {student[0]} ocjena: izvrstan(5)")
    
    elif bodovi <90 and bodovi >= 80:
        print(f"\nStudent {student[0]} ocjena: vrlodobar(4)")
    elif bodovi <80 and bodovi >= 65:
        print(f"\nStudent {student[0]} ocjena: dobar(3)")
    elif bodovi <65 and bodovi >= 50:
        print(f"\nStudent {student[0]} ocjena: dovoljan(2)")

    elif bodovi <65 and bodovi >= 0:
        print(f"\nStudent {student[0]} ocjena: nedovoljan(1)")
