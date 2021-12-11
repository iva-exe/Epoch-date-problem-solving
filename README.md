# Epoch-date-problem-solving
Epoch / date problem solving

Pokud data nesedí pamatuj, že datum je ve formátu "měsíc.den.rok" při zadávání.
Při výpisu jsou ale již dělaná podle lokálního času a jsou tak ve formátu "den.měsíc.rok".

Příkaz by měl být typu "-toepoch 1.8.22" což odkazuje na den 8. ledna 2022.

Z epochu poté můžete vytvořit discord zprávu s těmito fromamy - https://pastebin.com/rJFE9yxq

# What is epoch time?
The Unix epoch (or Unix time or POSIX time or Unix timestamp) is the number of seconds that have elapsed since January 1, 1970 (midnight UTC/GMT), not counting leap seconds (in ISO 8601: 1970-01-01T00:00:00Z). Literally speaking the epoch is Unix time 0 (midnight 1/1/1970), but 'epoch' is often used as a synonym for Unix time. Some systems store epoch dates as a signed 32-bit integer, which might cause problems on January 19, 2038 (known as the Year 2038 problem or Y2038). The converter on this page converts timestamps in seconds (10-digit), milliseconds (13-digit) and microseconds (16-digit) to readable dates.

Dle stránky https://www.epochconverter.com/

# Použitý postup v JS

Z data do epochu->
var myDate = new Date("July 1, 1978 02:30:00"); // Your timezone!
var myEpoch = myDate.getTime()/1000.0;
document.write(myEpoch);

Z epochu do data->
var myDate = new Date( your epoch date *1000);
document.write(myDate.toGMTString()+"<br>"+myDate.toLocaleString());

Dle stránky https://www.epochconverter.com/programming/#javascript
