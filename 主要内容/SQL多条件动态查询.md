# SQL多条件动态查询
----
----
![在这里插入图片描述](https://img-blog.csdnimg.cn/e8608d2df30446a58ddbdf34bb9d6dc5.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBATkpVU1RaSkM=,size_20,color_FFFFFF,t_70,g_se,x_16)

```xml
 <where>
            <if test=" status != null">
                status = #{status}
            </if>
            <if test="brandName != null and brandName != ''">
                and brand_name like #{brandName}
            </if>
            <if test = "companyName != null and companyName != ''">
                and company_name like #{companyName};
            </if>

        </where>
```

