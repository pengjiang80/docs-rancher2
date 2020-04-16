---
title: 访问和共享
---

如果您是 RKE 模板所有者，则可以与用户或用户组共享该模板，然后用户组可以使用该模板创建集群。

由于 RKE 模板是专门与用户和组共享的，因此所有者可以与不同的用户集共享不同的 RKE 模板。

共享模板时，每个用户可以有两个访问级别之一：

- **所有者：** 此用户可以更新、删除和共享其拥有的模板。所有者还可以与其他用户共享模板。
- **用户：** 这些用户可以使用模板创建集群。他们还可以将这些集群升级到同一模板的新版本。当您将模板共享为 **公开（只读）时**，Rancher 中的所有用户都具有该模板的用户访问权限。

如果用户创建了模板，则会自动成为该模板的所有者。

如果要委派更新模板的责任，可以共享模板的所有权。有关所有者如何修改模板的详细信息，请参阅[有关修改模板的文档](/docs/admin-settings/rke-templates/creating-and-revising/_index)。

有几种共享模板的方法：

- 在模板创建期间将用户添加到新的 RKE 模板
- 将用户添加到现有 RKE 模板
- 将 RKE 模板公开，与 Rancher 设置中的所有用户共享
- 与受信任的用户共享模板所有权

## 与指定用户或组共享模板

要允许用户或组使用模板创建集群，您可以为用户提供模板的基本**用户**访问级别。

1. 在**全局**视图中，单击**工具 > RKE 模板**。
1. 转到要共享的模板，然后单击**垂直省略号(…)>编辑**。
1. 在**共享模板**部分，单击**添加成员**。
1. 在**名称**字段中搜索要与之共享模板的用户或组。
1. 选择**用户**访问类型。
1. 单击**保存**。

**结果：** 用户或组可以使用模板创建集群。

## 与所有用户共享模板

1. 在**全局**视图中，单击**工具 > RKE 模板**。
1. 转到要共享的模板，然后单击**垂直省略号(…) > 编辑**。
1. 在**共享模板下**，单击**公开（只读）**，然后单击**保存**。

**结果：** Rancher 中的所有用户都可以使用模板创建集群。

## 共享模板的所有权

如果您是模板的创建者，则可能希望将维护和更新模板的责任委派给其他用户或组。

在这种情况下，可以为用户提供所有者类型的访问权限，该类型允许其他用户更新模板、删除模板或与其他用户共享对模板的访问权限。

要授予用户或组所有者访问权限，

1. 在**全局**视图中，单击**工具 > RKE 模板**。
1. 转到要共享的 RKE 模板，然后单击**垂直省略号(…)>编辑**。
1. 在**共享模板**下，单击**添加成员**，然后在**名称**字段中搜索要共享模板的用户或组。
1. 在**访问类型**字段中，单击**所有者**。
1. 单击**保存**。

**结果：** 具有所有者访问类型的用户或组，可以修改、共享或删除模板。