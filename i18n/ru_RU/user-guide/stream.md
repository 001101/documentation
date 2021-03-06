# Поток

Поток в EspoCRM - это определенная платформа, где вы можете увидеть обновления и новости для записей, которые вам интересны. Вы также можете публиковать свой собственный поток и сообщения для других пользователей (начиная с версии 3.8.0). В EspoCRM есть два вида потоков: поток записи и пользовательский поток.

По умолчанию следующие объекты имеют поток: учетные записи, контакты, возможности, случаи. Администраторы могут включать или отключать поток для определенного объекта в [Entity Manager](../administration/entity-manager.md).

## Поток записи

Поток записи отображается на панели «Stream» в виде определенной записи и информации касаемой ее. Здесь размещаются сообщения, обновления и новости, связанные с текущей записью.

## Пользовательский поток

Пользователи могут видеть свой поток в списке dashlet, а также на вкладке Stream. Пользователи также могут видеть потоки других пользователей в подробной информации, если у них есть доступ, который контролируется полем `Согласие пользователя`.

В потоке пользователя вы можете видеть сообщения, обновления и новости, связанные с записями, которые были сделаны определенным пользователем. Вы также можете видеть сообщения, которые адресованные пользователю. Эти сообщения не связаны ни с одной записью.

## Уведомления

Вы получите уведомления о новых дополнениях к вашему потоку, которые были добавлены другими пользователями.

## Сообщения

Вы можете создать сообщение, связанное с определенной записью. Вы также можете прикрепить файлы и изображения к своему сообщению. Если вы хотите упомянуть кого-то в своем посте, вам нужно просто набрать символ `@` и ввести имя пользователя. Пользователь, о котором вы упомянули в своем сообщении, будет уведомлен об этом.

## Сообщения для пользователей

_Эта функция доступна с версии 3.8.0._

Пользователи могут создавать сообщения для определенных пользователей, для определенных команд, для всех пользователей и для себя. Доступ к этой возможности контролируется полем `Разрешение на назначение` ролей.

## Фильтрация

Вы можете включить фильтр и видеть только те новости, которые вам интересны в потоке: `Все`, `Сообщения` или `Обновления`.
