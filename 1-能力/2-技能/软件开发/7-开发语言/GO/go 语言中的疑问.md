# go json序列化转义符的问题
问题：invalid character 'd' in string escape code
解决方案：问题的直接原因是：字符串转义码中的无效字符“d”， 查看待转换字符串中的转移字符串使用问题；

# go channel取值表达式中ok的用法
1.当管道已关闭，且管道中的数据已消费完时，返回false；
2.使用无缓冲管道时，要有消费者等待时，生产者才会手递手传递数据；

