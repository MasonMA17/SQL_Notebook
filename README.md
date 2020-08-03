# SQL_Notebook
SELECT DISTINCT tb_column FROM tb ###删除重复行，可以看有几类
SELECT DISTINCT tb_column,tb_column From tb  ###可以多列一起用
SELECT column FROM tb where IS NULL #####想看null行的时候用‘is null' or 'is not null'
SELECT product_type,COUNT(*)  FROM Product GROUP BY product_type ####按组分类计数
SELECT product_type, product_name,sale_price FROM product AS P1 WHERE sale_price>(SELECT AVG(sale_price) FROM Product AS P2 WHERE P1.product_type=P2.product_type GROUP BY product_type)   ####在同一商品种类中对各商品的销售单价和平均单价进行比较
