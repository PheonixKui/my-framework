# 从零写JavaWeb框架第一章

### 访问WEB-INF目录中的JSP文件

1. 方法1：   

  本来WEB-INF中的jsp就是无法通过地址栏访问的.所以安全.
  如果说你要访问这个文件夹中的jsp文件需要在项目的web.xml文件中去配置servlet格式。如下:

    `<servlet>
     <servlet-name>runtain</servlet-name>
     <jsp-file>/WEB-INF/INF.jsp</jsp-file>
     </servlet>
     <servlet-mapping>
     <servlet-name>runtain</servlet-name>
     <url-pattern>/XXX</url-pattern>
     <／servlet-mapping>`

2. 方法2：

    jsp内部转发    
   `<jsp:forward page ="/WEB-INF/jsp/test/test.jsp" />`

3. 方法3：  

    servlet内部转发    
`request.getRequestDispatcher("/WEB-INF/a.jsp").forward(request,response);`
