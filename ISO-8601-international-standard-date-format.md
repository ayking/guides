
# ISO 8601 international standard date format

|Symbol|Meaning|Kind|Example|
|------|-------|----|-------|
|D|day in year|(Number)|189|
|E|day of week|(Text)|E/EE/EEE:Tue, EEEE:Tuesday, EEEEE:T|
|F|day of week in month|(Number)|2 (2nd Wed in July)|
|G|era designator|(Text)|AD|
|H|hour in day (0-23)|(Number)|0|
|K|hour in am/pm (0-11)|(Number)|0|
|L|stand-alone month|(Text)|L:1 LL:01 LLL:Jan LLLL:January LLLLL:J|
|M|month in year|(Text)|M:1 MM:01 MMM:Jan MMMM:January MMMMM:J|
|S|fractional seconds|(Number)|978|
|W|week in month|(Number)|2|
|Z|time zone (RFC 822)|(Time Zone)|Z/ZZ/ZZZ:-0800 ZZZZ:GMT-08:00 ZZZZZ:-08:00|
|a|am/pm marker|(Text)|PM|
|c|stand-alone day of week|(Text)|c/cc/ccc:Tue, cccc:Tuesday, ccccc:T|
|d|day in month|(Number)|10|
|h|hour in am/pm (1-12)|(Number)|12|
|k|hour in day (1-24)|(Number)|24|
|m|minute in hour|(Number)|30|
|s|second in minute|(Number)|55|
|w|week in year|(Number)|27|
|y|year|(Number)|yy:10 y/yyy/yyyy:2010|
|z|time zone|(Time Zone)|z/zz/zzz:PST zzzz:Pacific Standard Time|
|'|escape for text|(Delimiter)|'Date=':Date=|
|''|single quote|(Literal)|'o''clock':o'clock|



a: AM/PM

A: 0~86399999 (Millisecond of Day)

c/cc: 1~7 (Day of Week)

ccc: Sun/Mon/Tue/Wed/Thu/Fri/Sat

cccc: Sunday/Monday/Tuesday/Wednesday/Thursday/Friday/Saturday

d: 1~31 (0 padded Day of Month)

D: 1~366 (0 padded Day of Year)

e: 1~7 (0 padded Day of Week)

E~EEE: Sun/Mon/Tue/Wed/Thu/Fri/Sat

EEEE: Sunday/Monday/Tuesday/Wednesday/Thursday/Friday/Saturday

F: 1~5 (0 padded Week of Month, first day of week = Monday)

g: Julian Day Number (number of days since 4713 BC January 1)

G~GGG: BC/AD (Era Designator Abbreviated)

GGGG: Before Christ/Anno Domini

h: 1~12 (0 padded Hour (12hr))

H: 0~23 (0 padded Hour (24hr))

k: 1~24 (0 padded Hour (24hr)

K: 0~11 (0 padded Hour (12hr))

L/LL: 1~12 (0 padded Month)

LLL: Jan/Feb/Mar/Apr/May/Jun/Jul/Aug/Sep/Oct/Nov/Dec

LLLL: January/February/March/April/May/June/July/August/September/October/November/December

m: 0~59 (0 padded Minute)

M/MM: 1~12 (0 padded Month)

MMM: Jan/Feb/Mar/Apr/May/Jun/Jul/Aug/Sep/Oct/Nov/Dec

MMMM: January/February/March/April/May/June/July/August/September/October/November/December

q/qq: 1~4 (0 padded Quarter)

qqq: Q1/Q2/Q3/Q4

qqqq: 1st quarter/2nd quarter/3rd quarter/4th quarter

Q/QQ: 1~4 (0 padded Quarter)

QQQ: Q1/Q2/Q3/Q4

QQQQ: 1st quarter/2nd quarter/3rd quarter/4th quarter

s: 0~59 (0 padded Second)

S: (rounded Sub-Second)

u: (0 padded Year)

v~vvv: (General GMT Timezone Abbreviation)

vvvv: (General GMT Timezone Name)

w: 1~53 (0 padded Week of Year, 1st day of week = Sunday, NB: 1st week of year starts from the last Sunday of last year)

W: 1~5 (0 padded Week of Month, 1st day of week = Sunday)

y/yyyy: (Full Year)

yy/yyy: (2 Digits Year)

Y/YYYY: (Full Year, starting from the Sunday of the 1st week of year)

YY/YYY: (2 Digits Year, starting from the Sunday of the 1st week of year)

z~zzz: (Specific GMT Timezone Abbreviation)

zzzz: (Specific GMT Timezone Name)

Z: +0000 (RFC 822 Timezone)
