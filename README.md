# Java Scala comments template


## 一、Javadoc tag

- 块标签：`@tag`
    - `@author author-info`：注释作者信息。
    - `@deprecated`：表示此API已废弃。
    - `@exception exception-class exception-description`：注释异常信息（可能出现的）。
    - `@param param-name param-description`：注释参数信息。
    - `@return description`：注释返回信息。
    - `@see reference`：引用注释（文本、链接、包、类等等）。
    - `@serial field-description|include|exclude`：序列化注释。
    - `@serialData data-description`：序列化数据注释。
    - `@serialField field-name field-type field-description`：序列化字段注释。
    - `@since datatime-text|version-text`：注释已存在的时间
    - `@throws exception-class exception-description`：注释异常信息（方法声明的）。
    - `@version version-info`：注释版本信息。
- 内联标签：`{@tag}`
    - `{@code code-text}`：注释代码文本
    - `{@docRoot}`：表示从任何生成的页面到生成的文档（目标）根目录的相对路径。
    - `{@inheritDoc}`：从最近的可继承类或实现接口复制注释文档到当前注释。
    - `{@link package.class#member label}`：链接引用文档。
    - `{@linkplain package.class#member label}`：链接引用文档。
    - `{@literal text}`：注释文本不需要转义HTML的<>。
    - `{@value package.class#field}`：注释常量值。

## 二、tag order

```java
/**
 * @author
 * @version
 * @param
 * @return
 * @throws
 * @exception
 * @see
 * @since
 * @serial
 * @serialField
 * @seriaData
 * @deprecated
 */
```

## 三、Javadoc template

### 1. package

```java
/**
 * packaage simple description.
 *
 * package detailed description
 * @author Eddie Wei
 * @see (optional)
 * @since (optional)
 * @CreateTime: ${YEAR}-${MONTH}-${DAY} 
 * @version (required)
 */
```

### 2. class and interface

```java
/**
 * class/interface simple description.
 *
 * class/interface detailed description

 * @author Eddie Wei
 * @see (optional)
 * @since (optional)
 * @CreateTime: ${YEAR}-${MONTH}-${DAY} 
 * @version (required)
 */
```

### 3. field

```java
/**
 * type simple description.
 *
 * type detailed description

 * @see  (optional)
 * @since  (optional)
 * @serialField | @serial  (optional)
 * @deprecated  (optional)
 */
```

### 4. method

```java
/**
 * type simple description.
 *
 * type detailed description

 * @author  (optional)
 * @CreateTime: ${YEAR}-${MONTH}-${DAY} 
 * @param  (optional)
 * @return  (optional)
 * @throws  (optional)
 * @exception  (optional)
 * @see  (optional)
 * @since  (optional)
 * @serialData  (optional)
 * @deprecated  (optional)
 */
```

**Reference**

1. [How to Write Doc Comments for the Javadoc Tool](https://www.oracle.com/technetwork/java/javase/documentation/index-137868.html#tag)
