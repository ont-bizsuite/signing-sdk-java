# signing-sdk-java

## signing方法说明

### 获取对象实例并设置signing-server服务地址
```
getInstance(String restfulUrl)
```

### 初始化设置app域名和签名私钥
```
init(String domain, String wif)
```

### 设置区块链节点
```
setBlockChainUrl(String blockChainUrl)
```

### 构建交易参数(非上链类型)
```
constructMessage(List<Map<String, Object>> argsList)
```

### 构建交易参数(上链类型)
```
constructTransaction(String contractHah, String method, List<Map<String, Object>> argsList, String payerAddress, Long gasLimit, Long gasPrice)
```

### 向signing-server获取二维码参数
```
invoke(String action, String id)
```

### 向signing-server查询验签结果
```
invokeResult(String id)
```

### 对数据签名
```
sign(String data)
```

### 验证签名
```
verifySignature(String ontId, String signedTx)
```

### payer签名
```
signPayer(String signedTx)
```

### 发送交易
```
sendTransaction(String signedTx)
```

### 发送预执行交易
```
sendPreExecTransaction(String signedTx)
```

### 查询交易事件
```
checkEvent(String hash)
```

## 中心化Ont ID方法说明

### 获取对象实例
```
getInstance()
```

### 初始化生成ONT ID的两个私钥
```
init(String wif1, String wif2)
```

### 注册ONT ID
```
registerOntId(Integer index)
```

### 获取ONT ID
```
getOntId(Integer index)
```

### ONT ID签名
```
ontIdSign(Integer index, String message)
```

### 构造二维码参数
```
generateQrCode(String id, Long expire, String callbackUrl, String dataUrl, String signature, Boolean mainNet)
```

### 构造添加owner的交易参数
```
addOwnerParams(Integer index)
```

### 添加owner交易上链
```
addOwner(Integer index, String ontId)
```

### 构造删除owner的交易参数
```
removeOwnerParams(Integer index)
```

### 删除owner交易上链
```
removeOwner(Integer index, String ontId)
```