import random

def get_random_quote():
    quotes = [
        "The only limit to our realization of tomorrow is our doubts of today. - Franklin D. Roosevelt",
        "The future belongs to those who believe in the beauty of their dreams. - Eleanor Roosevelt",
        "Do not watch the clock. Do what it does. Keep going. - Sam Levenson",
        "Keep your face always toward the sunshine—and shadows will fall behind you. - Walt Whitman",
        "The best way to predict the future is to invent it. - Alan Kay"
    ]
    return random.choice(quotes)

# Получение случайной цитаты
print(get_random_quote())
