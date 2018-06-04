# layui_expand
对layui tree 拓展异步加载，添加操作按钮功能
 layui.tree({
                elem: '#goodsType', //传入元素选择器
                url: environment.sysmanagementPrefix + "/tbConfigDict/queryByParentCode",
                method: 'get',
                token: BaseUtil.getToken(),
                btn:
                    {
                        del: {
                            fun: function (node, e) {
                            }
                            ,
                            name: "删除"
                        }
                        ,
                        edit: {
                            fun: function (node, e) {
                            }
                            ,
                            name: '修改'
                        }
                        ,
                        add: {
                            fun: function (node, e) {
                            }
                            ,
                            name: '添加'
                        }
                    }
                , nodes:
                    [{ //节点
                        name: '商品分类',
                        code: 'role_type',
                        showBtn: true
                    }]
            });