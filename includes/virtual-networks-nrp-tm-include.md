## 流量管理器配置文件
使用流量管理器及其子终结点资源可将流量分配到 Azure 内部和 Azure 外部的终结点。此类流量分配由策略控制。使用流量管理器还能监视终结点的运行状况，并根据终结点的运行状况重定向流量。

流量管理器配置文件的关键属性包括：

- **流量路由方法** - 可能的值包括“性能”、“加权”和“优先级”。
- **DNS 配置** - 配置文件的 FQDN。
- **协议** - 监视协议，可能的值为 *HTTP* 和 *HTTPS*。
- **端口** - 监视端口。 
- **路径** - 监视路径。
- **终结点** - 终结点资源的容器。

### 终结点 
终结点是流量管理器配置文件的子资源。它表示要根据流量管理器配置文件资源中配置的策略，将用户流量分配到的服务或 Web 终结点。

终结点的关键属性包括：
 
- **类型** - 终结点的类型，可能的值为“Azure 终结点”、“外部终结点”和“嵌套终结点”。 
- **目标资源 ID** – 服务或 Web 终结点的公共 IP 地址。这可能是 Azure 或外部终结点。
- **权重** - 流量管理中使用的终结点权重。 
- **优先级** - 用于定义故障转移操作的终结点优先级。 

<!---HONumber=76-->