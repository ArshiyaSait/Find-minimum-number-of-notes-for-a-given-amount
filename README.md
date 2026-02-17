# Find-minimum-number-of-notes-for-a-given-amount
def no_notes(a):
    Q = [500, 200, 100, 50, 20, 10]
    x = 0
    for q in Q:
        x += a // q
        a = a % q
    if a > 0:
        x = -1
    return x
print(no_notes(500))  # 1 note
print(no_notes(560))  # -1 because 560 cannot be made using available notes

OUTPUT:
1
-1

