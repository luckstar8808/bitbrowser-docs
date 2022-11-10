---
description: 分组创建、修改等接口文档
---

# 分组接口

{% swagger method="post" path="group/list" baseUrl="/" summary="分组list" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="page" type="Int" required="true" %}
分页，从0开始
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pageSize" type="Int" required="true" %}
分页条数，例如10
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="group/add" baseUrl="/" summary="添加分组" %}
{% swagger-description %}
添加分组
{% endswagger-description %}

{% swagger-parameter in="body" name="groupName" required="true" type="String" %}
分组名称
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sortNum" type="Int" %}
排序
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="group/edit" baseUrl="/" summary="修改分组" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}
分组id
{% endswagger-parameter %}

{% swagger-parameter in="body" name="groupName" required="true" %}
分组名称
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sortNum" type="Int" %}
排序
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="group/delete" baseUrl="/" summary="删除分组" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
分组id
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="group/detail" baseUrl="/" summary="分组详情" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
分组id
{% endswagger-parameter %}
{% endswagger %}
