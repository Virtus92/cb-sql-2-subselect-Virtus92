[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=18017227&assignment_repo_type=AssignmentRepo)
# SQL2_Subselect

# Zeichenkettenfunktionen

## Wichtige Zeichenkettenfunktionen

| Funktion  | Beispiel                           | Ergebnis                                               |
|-----------|------------------------------------|--------------------------------------------------------|
| `DECODE`  | `DECODE(GRADE, 'A', 4, 'B', 3, 'C', 2, 'D', 1, 0)` | Übersetzt die Char-Werte von `GRADE` in numerische Werte |
| `INITCAP` | `INITCAP(ENAME)`                   | Erster Buchstabe von `ENAME` groß                      |
| `INSTR`   | `INSTR(LOC, ' ')`                  | Ermittelt die Position des ersten Blanks in `LOC`      |
| `LENGTH`  | `LENGTH(ENAME)`                    | Anzahl von Zeichen in `ENAME`                          |
| `LOWER`   | `LOWER(ENAME)`                     | `ENAME` in Kleinbuchstaben                             |
| `SOUNDEX` | `SOUNDEX('SMYTH')`                 | Ermittelt einen Wert, der wie `SMYTH` klingt           |
| `SUBSTR`  | `SUBSTR(ENAME, 1, 2)`              | Ergibt 2 Zeichen von `ENAME` beginnend beim ersten Zeichen |
| `UPPER`   | `UPPER(ENAME)`                     | `ENAME` in Großbuchstaben                              |

## Beispiele

### Beispiel 1

```sql
SELECT INITCAP(ENAME) 
FROM EMP
WHERE UPPER(ENAME) = 'WARD';
```

### Beispiel 2

```sql
SELECT ENAME, JOB, DECODE(JOB, 'CLERK', 1, 'MANAGER', 3, 'PRESIDENT', 5, 2) AS JOB_CLASS
FROM EMP;
```

| ENAME  | JOB       | JOB_CLASS |
|--------|-----------|-----------|
| SMITH  | CLERK     | 1         |
| ALLEN  | SALESMAN  | 2         |
| WARD   | SALESMAN  | 2         |
| JONES  | MANAGER   | 3         |
| MARTIN | SALESMAN  | 2         |
| BLAKE  | MANAGER   | 3         |
| CLARK  | MANAGER   | 3         |
| SCOTT  | ANALYST   | 2         |
| KING   | PRESIDENT | 5         |
| TURNER | SALESMAN  | 2         |
| ADAMS  | CLERK     | 1         |
| JAMES  | CLERK     | 1         |
| FORD   | ANALYST   | 2         |
| MILLER | CLERK     | 1         |
