# Mybatis中单条件动态查询
----
----

```xml
<select id="selectBySingleCondition" resultMap="resultBrand">
        select * from tb_brand
        <where>
            <choose>

                <when test="status != null">
                    status = #{status}
                </when>

                <when test="brandName != null and brandName != ''">
                    brand_name like #{brandName}
                </when>

                <when test="companyName != null and companyName != ''">
                    company_name like #{companyName}
                </when>

            </choose>
        </where>
    </select>
```

==choose 相当于switch
when 相当于case==
