# `Sonolus-Version`

`Sonolus-Version`代表了這個伺服器所支持的Sonolus程式版本。

## 語法

```http
Sonolus-Version: <value>
```

## 例子

```http
Sonolus-Version: 0.5.0
```

## 備註

當玩家嘗試利用一個不支持版本的Sonolus程式加入伺服器時，會出現一個通知玩家的彈窗畫面，並會取消他的輸入。

雖然並不強制使用，但仍然強烈建議加入這個標頭，以確保使用這個伺服器的玩家能獲取最佳的遊戲體驗。
