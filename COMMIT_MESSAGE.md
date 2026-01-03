# Git Commit Message / Git 提交信息

## English Version / 英文版本

```
Fix SQL injection vulnerabilities and improve input sanitization

Security Fixes:
- Replace direct SQL concatenation with $wpdb->prepare() in domain existence checks (line 350)
- Replace direct SQL concatenation with $wpdb->prepare() in DELETE query (line 380)
- Replace esc_sql() + direct concatenation with $wpdb->prepare() in HTTP_HOST query (line 519)
- Replace direct SQL concatenation with $wpdb->prepare() in primary domain query (line 526)
- Replace direct SQL concatenation with $wpdb->prepare() in domain list query (line 444)
- Replace esc_sql() with sanitize_text_field() for better input sanitization (lines 341, 374)

All SQL queries now use prepared statements following WordPress coding standards,
which prevents SQL injection attacks and ensures better security.

Input sanitization improvements:
- Use sanitize_text_field() instead of esc_sql() for form inputs
- Provides better XSS protection and HTML tag removal
- Recommended by WordPress coding standards

Changes:
- Line 341: Replace esc_sql() with sanitize_text_field() for POST input
- Line 350: Use $wpdb->prepare() for domain existence checks
- Line 374: Replace esc_sql() with sanitize_text_field() for GET input
- Line 380: Use $wpdb->prepare() for DELETE operations
- Line 444: Use $wpdb->prepare() for domain list retrieval
- Line 519: Use $wpdb->prepare() for HTTP_HOST domain lookup
- Line 526: Use $wpdb->prepare() for primary domain retrieval

This update maintains backward compatibility while significantly improving security.
```

## Chinese Version / 中文版本

```
修复 SQL 注入漏洞并改进输入清理

安全修复：
- 在域名存在性检查中使用 $wpdb->prepare() 替换直接 SQL 拼接（第350行）
- 在 DELETE 查询中使用 $wpdb->prepare() 替换直接 SQL 拼接（第380行）
- 在 HTTP_HOST 查询中使用 $wpdb->prepare() 替换 esc_sql() + 直接拼接（第519行）
- 在主域名查询中使用 $wpdb->prepare() 替换直接 SQL 拼接（第526行）
- 在域名列表查询中使用 $wpdb->prepare() 替换直接 SQL 拼接（第444行）
- 使用 sanitize_text_field() 替换 esc_sql() 以获得更好的输入清理（第341、374行）

所有 SQL 查询现在都使用预处理语句，遵循 WordPress 编码规范，
可防止 SQL 注入攻击并确保更好的安全性。

输入清理改进：
- 对表单输入使用 sanitize_text_field() 而不是 esc_sql()
- 提供更好的 XSS 防护和 HTML 标签去除
- 符合 WordPress 编码规范推荐

变更内容：
- 第341行：POST 输入使用 sanitize_text_field() 替换 esc_sql()
- 第350行：域名存在性检查使用 $wpdb->prepare()
- 第374行：GET 输入使用 sanitize_text_field() 替换 esc_sql()
- 第380行：DELETE 操作使用 $wpdb->prepare()
- 第444行：域名列表检索使用 $wpdb->prepare()
- 第519行：HTTP_HOST 域名查找使用 $wpdb->prepare()
- 第526行：主域名检索使用 $wpdb->prepare()

此更新在保持向后兼容性的同时显著提高了安全性。
```

## Short Version (for git commit -m) / 简短版本（用于 git commit -m）

### English / 英文
```
Fix SQL injection vulnerabilities and improve input sanitization
```

### Chinese / 中文
```
修复 SQL 注入漏洞并改进输入清理
```

## Combined Bilingual Version / 中英双语合并版本

```
Fix SQL injection vulnerabilities and improve input sanitization
修复 SQL 注入漏洞并改进输入清理

Security Fixes / 安全修复:
- Line 341: Replace esc_sql() with sanitize_text_field() for POST input
  第341行：POST 输入使用 sanitize_text_field() 替换 esc_sql()
- Line 350: Use $wpdb->prepare() for domain existence checks
  第350行：域名存在性检查使用 $wpdb->prepare()
- Line 374: Replace esc_sql() with sanitize_text_field() for GET input
  第374行：GET 输入使用 sanitize_text_field() 替换 esc_sql()
- Line 380: Use $wpdb->prepare() for DELETE operations
  第380行：DELETE 操作使用 $wpdb->prepare()
- Line 444: Use $wpdb->prepare() for domain list retrieval
  第444行：域名列表检索使用 $wpdb->prepare()
- Line 519: Use $wpdb->prepare() for HTTP_HOST domain lookup
  第519行：HTTP_HOST 域名查找使用 $wpdb->prepare()
- Line 526: Use $wpdb->prepare() for primary domain retrieval
  第526行：主域名检索使用 $wpdb->prepare()

All SQL queries now use prepared statements following WordPress coding standards,
which prevents SQL injection attacks and ensures better security.

所有 SQL 查询现在都使用预处理语句，遵循 WordPress 编码规范，
可防止 SQL 注入攻击并确保更好的安全性。

Input sanitization improvements:
- Use sanitize_text_field() instead of esc_sql() for form inputs
- Provides better XSS protection and HTML tag removal
- Recommended by WordPress coding standards

输入清理改进：
- 对表单输入使用 sanitize_text_field() 而不是 esc_sql()
- 提供更好的 XSS 防护和 HTML 标签去除
- 符合 WordPress 编码规范推荐
```

