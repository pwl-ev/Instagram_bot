a bot that automatically subscribes to accounts and puts likes.

Бот, который автоматически подписывается на аккаунты и ставит лайки.

Инструкция:

Ссылки на аккаунты мы берем со страницы тех кто ставил "сердечки" какой-либо из фотографий.

Ссылку на пост принимает функция write_to_file(). Ссылка должна иметь следующий вид "https://www.instagram.com/p/CjTYJA9P2TN/". Чтобы получить ссылку в таком виде нам нужно нажать на "..." в верхнем правом углу над фотографией и нажать "Перейти к публикации". Даеле просто скопировать ссылку из браузера.

Все ссылки будут записаны в файл accounts.txt, после чего нам надо будет запустить функцию reading_from_file(). Во время работы этой функции ссылки будут построчно удалятся и записываться в файл "to_unscribe.txt", для того чтобы в дальнейшем можно было отписаться от всех аккаунтов на которые мы подписывались. (В данный момент этот функционал еще не реализован).

После подписки на аккаунт мы открываем 2 фотографии из аккаунта и ставим им лайк (при условии что в аккаунте >= 2 фотографии и аккааунт открытый).

Для авторизации вам необходимо ввести ваш username и password в файле config.py либо при запуске программа сама попропист вас их ввести. В данный момент реализован вход только непосредственно через сам instagram, в дальнейшем будет добавлена возможность авторизации через facebook.

Примечание: За одно выполнение функции write_to_file() мы получаем максимум 102 ссылки на аккаунты (что по слухам равно суточному лимиту на подписки). Паузы между подписками установлены в диапазоне от 90 до 150 секунд. В среднем мы получаем +/- 35 подписок в час. Аккаунты на которые мы уже подписаны - игнорируются. Если вы хотите получить больше ссылок запустите функцию write_to_file() повторно, но уже с другой фотографией.

Почему я решил подписываться на аккаунты которые поставили лайки фоторграфии? Потому что по моим наблюдениям - это самая "теплая" и активная аудитория. Приблизительная конверсия в ответную подписку бота составляет 15%.

Если Вам потребуется помощь с запуском бота напишите мне на почту pwl93.e@gmail.com