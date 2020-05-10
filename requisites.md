---
layout: page
title: Платёжные реквизиты
permalink: /requisites/
lang: ru
exclude: true
Name: СРОО "Саратовский центр СПО"
PayeeINN: 6450101120
KPP: 645001001
PersonalAcc: 40703810856000002997
BankName: ПАО Сбербанк
BIC: 043601607
CorrespAcc: 30101810200000000607
Purpose: На уставную деятельность, НДС не облагается
Sum: 100000
---
* **Получатель**: {{page.Name}}
* **Банк**: {{page.BankName}}
* **Расчётный счёт**: {{page.PersonalAcc}}
* **ИНН получателя**: {{page.PayeeINN}}
* **БИК**: {{page.BIC}}
* **КПП**: {{page.KPP}}
* **Комментарий**: {{page.Purpose}}, &lt;Фамилия&gt;
(Фамилию можно не указывать)

{% capture QRText %}ST00011|Name={{page.Name}}|PayeeINN={{page.PayeeINN}}|KPP={{page.KPP}}|PersonalAcc={{page.PersonalAcc}}|BankName={{page.BankName}}|BIC={{page.BIC}}|CorrespAcc={{page.CorrespAcc}}|Purpose={{page.Purpose}}|Sum={{page.Sum}}{% endcapture %}
![QR Code](https://zxing.org/w/chart?cht=qr&chs=500x500&chld=L&choe=UTF-8&chl={{QRText | url_encode}})
