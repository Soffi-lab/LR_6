import sqlite3


# создание класса БД
class Chess:
    # конструктор класса
    def __init__(self):

                # Подключение к БД
                self.con = sqlite3.connect("Chess.db")
                # Создание курсора
                self.cur = self.con.cursor()
                # Создание таблицы БД
                self.cur.execute(
                "CREATE TABLE IF NOT EXISTS Sportman "
                "(ID INTEGER PRIMARY KEY,"
                "lastname_s TEXT,"
                "Date_of_Birth INTEGER,"
                "country TEXT,"
                "sports_category TEXT,"
                "Name TEXT,"
                "the_date_of_the INTEGER,"
                "busy_place INTEGER)"

                )
               self.con.commit()

def __del__(self):
  # отключение от БД
  self.con.close()

def view(self):
  # просмотр всех записей в таблице БД
  self.cur.execute("SELECT * FROM Sportman")
  # список всех записей из таблицы
  rows = self.cur.fetchall()
  return rows

def insert(self, lastname_s, Date_of_Birth, country,sports_category,Name,the_date_of_the,busy_place):
  # добавить запись
  self.cur.execute("INSERT INTO Sportman "
                  "VALUES (NULL, ?, ?, ?,?,?,?,?)",
                  (lastname_s, Date_of_Birth, country,sports_category,Name,the_date_of_the,busy_place,))
  self.con.commit()

def update(self, id, lastname_s, Date_of_Birth, country,sports_category,Name,the_date_of_the,busy_place):
    # редактирование записи
    self.cur.execute("UPDATE Sportman SET "
                    "lastname_s=?, Date_of_Birth=?, country=?,sports_category=?,Name=?,the_date_of_the=?,busy_place=? "
                    "WHERE ID = ?",
                    (lastname_s, Date_of_Birth,
                    country,sports_category,Name,the_date_of_the,busy_place, id,))
    self.con.commit()

def delete(self, id):
    # удаление записи
    self.cur.execute("DELETE FROM Sportman "
                    "WHERE ID=?", (id,))
    self.con.commit()

def search(self, lastname_s):
    self.cur.execute("SELECT Date_of_Birth, country,sports_category,Name,the_date_of_the,busy_place FROM Sportman "
                    "WHERE lastname_s=?", (lastname_s,))
    rows = self.cur.fetchall()
    return rows
