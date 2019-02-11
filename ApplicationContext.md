# Ubuntu 18.04♥中的TYPO3 —— 应用上下文

修改站点配置文件`/etc/nginx/conf.d/domain.tld.conf`

    server {
        ...
        location ~ \.php$ {
            fastcgi_param TYPO3_CONTEXT value;
        }
    }

可选值为`Development`、`Production/Staging`、`Production`。

重启Nginx

	service nginx restart

[<< 返回](README.md)