# Data Types  
  
CHAR String       (0 - 255)  
VARCHAR String    (0 - 255)  
TINYTEXT String   (0 - 255)  
TEXT String       (0 - 65535)   
BLOB String       (0 - 65535)  
MEDIUMTEXT String (0 - 16777215)  
MEDIUMBLOB String (0 - 16777215)  
LONGTEXT String   (0 - 4294967295)  
LONGBLOB String   (0 - 4294967295)  
TINYINT x Integer (-128 to 127)  
SMALLINT x Integer(-32768 to 32767)  
MEDIUMINT x Integer (-8388608 to 8388607)  
INT x Integer     (-2147483648 to 2147483647)  
BIGINT x Integer  (-9223372036854775808 to 9223372036854775807)  
FLOAT Decimal     (precise to 23 digits)  
DOUBLE Decimal    (24 to 53 digits)  
DECIMAL "DOUBLE" stored as string  
DATE              YYYY-MM-DD  
DATETIME          YYYY-MM-DD HH:MM:SS  
TIMESTAMP         YYYYMMDDHHMMSS  
TIME              HH:MM:SS  
ENUM              One of preset options  
SET               Selection of preset options  
  
# Mathematical Functions  
  
ABS     COS  
SIGN    SIN  
MOD     TAN  
FLOOR   ACOS  
CEILING ASIN  
ROUND   ATAN, ATAN2  
DIV     COT  
EXP     RAND  
LN      LEAST   
LOG, LOG2, LOG10 GREATEST   
POW     DEGREES   
POWER   RADIANS   
SQRT    TRUNCATE  
PI  
  
# Date and Time Functions  
  
DAYOFWEEK DATE_SUB  
WEEKDAY ADDDATE  
DAYOFMONTH SUBDATE  
DAYOFYEAR EXTRACT   
MONTH TO_DAYS  
DAYNAME FROM_DAYS  
MONTHNAME DATE_FORMAT  
QUARTER TIME_FORMAT  
WEEK CURRENT_DATE  
YEAR CURRENT_TIME  
YEARWEEK NOW  
HOUR SYSDATE  
MINUTE UNIX_TIMESTAMP  
SECOND FROM_UNIXTIME  
PERIOD_ADD SEC_TO_TIME  
PERIOD_DIFF TIME_TO_SEC  
DATE_ADD  
  
# Miscellaneous Functions  
  
BIT_COUNT    DES_ENCRYPT  
DATABASE     DES_DECRYPT  
USER LAST  _ INSERT_ID  
SYSTEM_USE   FORMAT  
SESSION_USER VERSION  
CURRENT_USER CONNECTION_ID  
PASSWORD     GET_LOCK  
OLD_PA­SSWORD RELEASE_LOCK  
ENCRYPT      IS_FREE_LOCK  
DECODE       BENCHMARK  
MD5          INET_NTOA  
SHA1         INET_ATON  
AES_ENCRYPT  FOUND_ROWS  
AES_DECRYPT  STRCMP  
  
# String Functions  
  
ASCII       SUBSTRING  
ORD         MID  
CONV        SUBSTRING_INDEX  
BIN         LTRIM  
OCT         RTRIM  
HEX         TRIM  
CHAR        SOUNDEX  
CONCAT      SPACE  
CONCAT_WS   REPLACE  
LENGTH      REPEAT  
CHAR_LENGTH REVERSE  
BIT_LENGTH  INSERT  
LOCATE      ELT  
INSTR       FIELD  
LPAD        LCASE  
RPAD        UCASE  
LEFT LOAD  _FILE  
RIGHT       QUOTE  
  
# Grouping Functions  
  
AVG           MAX  
BIT_AND       STD  
BIT_OR        STDDEV  
COUNT         SUM  
GROUP_CONCAT  VARIANCE  
MIN  


![Cheat Sheet1](assets/mysql_cheat_sheet1.png)

