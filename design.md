# logic

## if you have linepush or web

プレーヤーがいるグループにBotを入れる。

(in a group that all member plays)

user a: start
bot: ラウンド数を決めてください。
user a: X

if not approved line@
    bot: 参加者は参加を押してください。
    bot: 参加者を締め切る場合は、締め切るを押してください。
    bot: このメンバーで始めます。

bot: 初期化したくなったら、初期化と入力してください。

for round in range(X):
    single_turn()

    if last:
        bot: ゲームが終了しました。
        bot: スコアを表示します。

single_turn():
    bot: ではマスターを一人、庶民をa人、そしてインサイダー1人を決めます。
    bot: このグループにいる方に個別にメッセージを送りました。
    bot: 自分の役割と誰がマスターかを確認してください。
    bot: マスターとインサイダーにはお題も送りました。

    bot: マスターはBot個人メッセージ画面を開き、スタートを押してください。
    bot: それではお題を皆様当ててください。
    bot: お題が当てられたら、マスターはストップを押してください。

    ### お題あてる

        bot: お題が当てられストップが押されました。
        bot: マスターは再びスタートを押してください。
        bot: それでは、議論を誘導した狡猾なインサイダーを庶民の皆様は見つけてください。

        bot: 時間切れです。
        bot: 皆さん、インサイダーと思われる方を指定してください。

        user: （個人宛に来たものを返信）

        bot: インサイダーとして疑われたのはYYYです。
        bot: 実際はYYYは、、、、

        ### インサイダー的中
            bot: インサイダーでした。
            bot: インサイダー以外の皆様にはポイントが加わります

        ### インサイダーハズレ
            bot: 庶民でした。実のインサイダーはBBBでした。
            bot: インサイダーにはポイントが加算されます。

    ### お題あてられれず

        bot: 時間切れです。
        bot: インサイダーは庶民を誘導することに失敗しました。
        bot: 実際のインサイダーは、AAAでした。
        bot: お題は、CCCでした。
        bot: インサイダーAAAは減点となります。

    if round is not X:
        bot: 次のラウンドを開始します。


