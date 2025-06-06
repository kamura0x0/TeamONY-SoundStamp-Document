# SoundStamp 要件定義

## コア機能
1. 環境音 10 秒録音
   - MediaRecorder 固定長

2. オンデバイス AI 音分類
   - TF-JS (量子化 YAMNet)
> なんの音かAIが判断してラベルをつける

3. アイコン & カラーパレット自動決定
   - ラベル→絵文字＋16色
> AIが感じた音の印象を絵文字に変換して、それをカラーパレットに変換して、それをスタンプにして、それを地図にスタンプする

4. 地図スタンプ
   - Mapbox v2 LTS、クラスタリング
> 地図にスタンプする

5. スタンプ永続化 (認証なし)
   - Supabase Storage + stamps テーブル (anon insert/select)
> アプリを閉じてもスタンプが永続的に残る

6. 再生ビュー(録音した音の確認ページ的なやつ)
   - 波形＋削除/ラベル修正
> 録音した音を再生し, 音声を確認できる
> (どっちでもあり) ラベルを修正したり、削除したりできる

7. 時間帯(6h)・天気タグ自動付与
   - Open-Meteo
> 時間帯や天気をタグとしてつける
> 時間帯はNTPサーバーからフェッチして、天気は位置情報から何かしらのAPIからフェッチする
> (時間がかかりそうなら) ユーザーの自己申告制にする


### 時間があったらやりたいこと

8. 図鑑コレクション & デイリーチャレンジ
   - localStorage
> ブラッシュアップ機能

9. GIF/Deep-Link シェア
   - SNS 流入用
> ブラッシュアップ機能

## コンセプト
- 10秒の軌跡印 (メインコンセプト)
  - あなたの過ぎ去った10秒の軌跡を、地図に静かに印す。(サブコンセプト)

- 
## ユーザーターゲット

## 解決する課題
