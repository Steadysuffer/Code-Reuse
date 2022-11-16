# 1)функция, которая возвращает текущий баланс друга с именем name, исходя из списка транзакций transactions. Если имя
# name ни разу не встречается в списке transactions, считаем, что баланс этого друга в общаке равен 0 рублей.
# 2)функция, которая принимает список имен присутствующих на мероприятии друзей names, стоимость баранок и чая на
# человека amount, а также список транзакций в общак transactions. Вернуть эта функция должна словарь
# вида {"имя_друга": 100}, где 100 - это количество денег, которое он должен скинуть на мероприятие. Если на балансе
# друга больше денег, чем требуется на мероприятие, то он должен 0 рублей.

transactions = [{"name": "Василий", "amount": 500}, {"name": "Петя", "amount": 100}, {"name": "Василий", "amount": -300}]


def get_balance(name, transactions):
    balance = 0
    for i in transactions:
        if i.get("name") == name:
            balance = balance + i.get("amount")
    return balance


def count_debts(names, amount, transactions):
    many_debt = []
    for i in names:
        debt = amount - get_balance(i, transactions)
        if debt > 0:
            many_debt.append(debt)
        else:
            many_debt.append(0)
    dict1 = dict(zip(names, many_debt))
    return dict1


print(get_balance("Василий", transactions))
print(count_debts(["Василий", "Петя", "Вова"], 150, transactions))
