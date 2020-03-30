[fukuoka.ex／kokura.ex](https://fukuokaex.connpass.com/)のpiacereです
ご覧いただいて、ありがとうございます :bow:

テキサスで開催されたElixirカンファレンス[「Lonestar Elixir 2020」](https://lonestarelixir.com/)で、私が世界で2番目に尊敬するプログラマ、Dave Thomas（Twitter：[@pragdave](https://twitter.com/pragdave)）が登壇し、その模様が先日YouTubeに公開されたので、YouTube字幕の助けを借りながら文字起こしし、翻訳にトライしてみたいと思います

Dave Thomasは、私のプログラマ人生に、20年前からずっと良いインスピレーションを与え続けてくれている、今年で御年60歳（！）の現役凄腕プログラマです

日本のプログラマの皆さまに、彼のプログラミングに賭けるパッションを知ってもらえたらいいな ＆ 動画を紹介することでホンの少しでもこれまでの恩恵に報いることができたらいいな、と思っています

[<b>Lonestar Elixir 2020 Speaker Talks: Dave Thomas - How I'm Becoming a Programmer</b>](https://www.youtube.com/watch?v=sXXh16455LA)
https://www.youtube.com/watch?v=sXXh16455LA
[![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/bbd29368-ce07-ddd4-8ee6-18b2d25f4d2f.png)](https://www.youtube.com/watch?v=sXXh16455LA)

# 翻訳に際して

この登壇は48分あり、私がそこまで英語が達者で無いこともあるため、3～4回に分けて、文字起こし＆翻訳を進めたいと思います

なお、文字起こしが間違っている可能性はおおいにあるので、英語詳しい方、どうぞアドバイスやツッコミをください

あと翻訳については、「20年前から大好きな、Dave Thomas特有のノリ」を踏襲すべくアレンジしているところがありますが、意味が明らかに間違っているところがあれば、やはりアドバイスやツッコミをいただけたら幸いです

<b><font color="red">※ちなみにTwitterで「翻訳ツラタン」ってグチったら、ナントDave Thomas御本人降臨してしまった … 20年前、神としか思ってなかった存在に、思いも寄らず接近できてしまい、やはりTwitterは神の給うたツールとしか思えない ＆ なんて良い時代に自分は生まれたんだろう … 正直、本件は途中で何度もヘシ折れそうだったけど、最後まで頑張ろう</font></b>
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/39bcee4f-5156-dc53-a5b0-a1b23f8d2135.png)

# はじめに：私のプログラマ人生を変えたDave Thomas

<font color="silver">※下記書籍リンクは、読んだ当時版と、最新版の両方でお届けします</font>

20年前に彼の著書、<b>達人プログラマー [【旧版】](https://www.amazon.co.jp/exec/obidos/ASIN/4894712741/onelinebiz-22) [【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/427421933X/onelinebiz-22)</b>（The Pragmatic Programmer [【旧版】](https://www.amazon.co.jp/exec/obidos/ASIN/020161622X/onelinebiz-22) [【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/0135957052/onelinebiz-22)）を読んだことで、私のエンジニア人生は一変し、「eXtreme Programming」はじめとするアジャイル開発やTDD、CIといった、現代では当たり前だけど、20年前にはまったく当たり前で無い、素晴らしいプログラミング／エンジニアリングの世界に導かれました
[![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/ae0f3b3a-03dc-bf7f-f41a-927cb8ea539b.png)](https://www.amazon.co.jp/exec/obidos/ASIN/4894712741/onelinebiz-22)

その後、約13年前にやはり彼の著書、<b>RailsによるアジャイルWebアプリケーション開発 [【旧版】](https://www.amazon.co.jp/exec/obidos/ASIN/4274066401/onelinebiz-22) [【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/B07BDHD7YM/onelinebiz-22)</b>（Agile Web Development With Rails[【旧版】](https://www.amazon.co.jp/exec/obidos/ASIN/0977616630/onelinebiz-22) [【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/1680506706/onelinebiz-22)）を読み、当時、国内ではほとんど流行っていなかったRuby on Railsに衝撃を受け、フルスタックWeb＋CoCフレームワークの世界へと傾倒しました（業務のメインは、PHPやScalaでしたが、折に触れ紹介したり、自分の会社で使いました）
[![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/9c8fbaad-0415-f0f3-029f-5e61e3dc4e91.png)](https://www.amazon.co.jp/exec/obidos/ASIN/B07BDHD7YM/onelinebiz-22)

それから9年後、RubyKaigiで名前だけは聞いていたElixirを個人的に試していたところ、やはり彼の<b>プログラミングElixir[【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/4274219151/onelinebiz-22)</b>（Programming Elixir[【旧版】](https://www.amazon.co.jp/exec/obidos/ASIN/1680501666/onelinebiz-22)  [【新版】](https://www.amazon.co.jp/exec/obidos/ASIN/1680502999/onelinebiz-22)）に出会ったとき、雷に打たれる程の衝撃を受け、以来、アルケミストをしています
[![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/cbf3c257-2387-6334-a58d-f1ecd4dc98d0.png)](https://www.amazon.co.jp/exec/obidos/ASIN/4274219151/onelinebiz-22)

# 本編：司会のBruce TateからDave Thomasの紹介

(1:43～1:58)

I'd like to introduce Dave, What can I say beyond? None of us would be in this room without him.

So, the same attention that he gives to his book and his writing, I've seen him pour into students that it.

So, Dave Thomas.

---

デイブを紹介します。なんて紹介すればいいでしょうか。彼がいなければ、誰もこの会場には来なかったでしょう。

そして、彼の本と執筆に彼が向ける興味関心、私は彼がその興味関心を読者に投げかけるさまを見てきました。

それでは、デイブ・トーマス

# Dave Thomasの挨拶

(2:05～2:39)
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/d946a684-7133-52d9-1cae-a6e88af3c92a.png)

Wow, fantastic conference.

I'm not gonna I'm sure at the end.

We will have a nice summary.

So, I'm not gonna gush too much, but I must admit I always enjoy these conferences.

So, thank you to everybody involved.

How many people have seen me speak at a previous Elixir event?

(Notice: Maybe the audience is raising their hands)

Oh, for a number twice?

(Notice: Same here)

All right, so the ones that have seen me speak are kind of nervous right now, and the ones that see me speak twice are kind of wondering if they can get out of the room, because I kind of have a bit of a nasty habit.

---

ワォ、ファンタスティックなカンファレンスですね

私はそういうつもりはないけれど、私がこのカンファレンスの最後の登壇者だと思います

私たちはカンファレンスのまとめをしましょう

なので，あまりたくさんしゃべるつもりはありません、でも、私はいつもこれらのカンファレンスを楽しんでいることを認めます

関係するみなさん全員に感謝です

以前のElixirイベントで私が話すのを見た人は何人いますか？

（※訳者コメント：たぶん会場の参加者が手を挙げてると思います）

あぁ、2度目は？

（※訳者コメント：コチラも手を挙げてるでしょう）

了解しました。では、私が話すのを見たことがある人は、今、緊張していて、2回目の人達は、部屋を出ていかないのが不思議ですね、というのは、私はちょっと厄介な癖があるからです

# OTPは過大評価されています（OTP IS OVER RATED）

(2:40～3:07)
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/a8056907-0897-c2d3-ad7f-9bac88ce916c.png)

I tend to be the person that has talks like.

Oh, I don't know...

OTP is overrated we should we shouldn't be using OTP that much right do ourselves why not.

I can actually claim Joe Armstrong agrees with me on this, but no one's gonna contradict that.

---

私は、つい、（タイトルのような）こういう話をしちゃいます

あぁ、知らないですよ …

OTPは過大評価されているので、OTPを使用してはならないはずです

これにJoe Armstrong（訳者注：Erlang／OTPの作者です）が同意するよう仕向けることはできますが、誰も賛同はしないでしょう

# Phoeinxはモノリスだ（PHOENIX FAVORS MONOLITHS）

(3:10～3:24)
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/5ab3321f-2c05-250e-0113-b85042f2eff8.png)

Phoenix favors monoliths no one's gonna argue with that obviously.

But get in trouble people don't like that you know.

I'm sort of like you know attacking the gods and that doesn't go down well.

---

Phoeinxは、モノリシックなままですが、誰もそこにツッコミを入れません

しかし、あなたがそれを知っていることでトラブルになることは、誰も好んでません

あなたが「神々への攻撃を知っている」けど、それが上手くはいかないようなものです

# Webアプリは退屈（WEB APPS ARE BORING）

（3:29～4:20）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/ab165617-5624-f62a-6a8c-a8ddcec3a55f.png)

Our apps are boring if I see one more damn web app...

Oh, kill me come on.

Non web apps outweigh web apps by 3 orders of magnitude if you look at just processors.

There are a 1,000 times more processors in small devices than there are in browsers and that doesn't mean phones.

I mean smaller than the phones.

We have the best technology in the world for talking to those devices.

And yes, we do have some projects that are looking at there.

But as a community why we should be pushing up.

But I'm not gonna do that.

Cuz that would be that would be nasty and mean and I'm not nasty and mean.

And we are not Elixir programmers that one I'll defend to the hilt.

---

忌々しいもう1つのWebアプリとして、私達のアプリは退屈です …

あぁ、私を殺してくれ、さぁ

CPUの使い方で見ると、非Webアプリは、Webアプリより3桁は優れています

小さなデバイスには、ブラウザで使われるよりも、1,000倍以上のプロセッサが入っており、それは携帯電話を意味していません

携帯電話よりも小さいことを意味します

私達は、これらのデバイスと通信するための世界で最高のテクノロジーを持っています

もちろん、そこには幾つかのプロジェクトがあります

しかし、コミュニティとして、なぜ私達が押し上げるべきなのか？

私はやりません

それは、厄介で汚らわしいことになるだろうし、私は厄介で汚らわしくはありません

私達は、Elixirプログラマでは無いので、そのことを徹底的に守ります

# 私達はElixirプログラマでは無い（WE ARE NOT ELIXIR PROGRAMMERS）

（4:27～5:47）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/1ad5410d-cbfd-db6d-2b5f-4363d413f551.png)

I hate it when people say you know, you say to him well.

Okay, first of all this is an American thing right.

America is the only country, the U.S. is the only country in the world where the first thing you say to someone you've never met before at a party or something.

It's not How are you or that's a really nice haircut its.

What do you do?

Implicitly how much do you make?

Because then I can judge myself against you, right?

(Translator's comment: I can't hear the audience reply...)

You do? okay.

---

「あなたは（Elixirを）知っている」とみんなが言うとき、私はそれを嫌います

OK、まずこれはアメリカでのことです

アメリカは世界で唯一、パーティーなどで会ったことのない人に、最初に話しかける国です

「お元気ですか？（もしくは）本当に素敵な髪型ですね？

お仕事は何ですか？

実は、どのくらい稼いでますか？」

これで私は、あなたを判断することができます … だよね？

(訳者コメント：観客からの返事が聞き取れない…)

あなたがやる？OK

---

You know I hate to say it but I think that makes my point.

You are not an Elixir developer.

You are a developer but more to the point you were problem solver and you're someone this change in the world stop calling yourself an Elixir programmer.

All right, so, you see I can use one that.

Yes! so, the problem is I keep giving these talks and I've done like 5 or 6 of these talks of various Elixir events and I and up with an audience looking at me like that.

---

あなたが、こう言われることを嫌いなことは知っていますが、私は言います

あなたはElixirデベロッパーではありません

あなたは開発者なのですが、「問題を解決する人」であり、あなたは何らかの世界の変化に伴い、あなた自身をElixirプログラマと呼ぶことを止めました

オーライ、あなたは、私がそう言うのを見ています

そう、問題は、私がこれらの講演を続けており、様々なElixirイベントで5～6回、お話してきたことで、私ももう、私を見ている観客と同じ気分です

# もうウンザリだ…（I'm sick of it…）

（5:48～6:01）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/47f22338-289e-34c4-e10a-0cb704a0d721.png)

And I had to put that in everybody else's had pictures of their pet or their whatever else. (Translator's comment: What does this mean?)

I'm sick of it...

I'm sick of it...

Because I am not that kind of person all right.

---

そして、誰かの持っているペットや何かの写真に入れなければなりませんでした …（訳者コメント：この言い回しとここの前後の流れはよく分からない…会場は湧いてるが）

もうウンザリだ…

もうウンザリだ…

私はそんな人じゃないから

# これは私です（That's me）

（6:02～6:09）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/84c19fa7-0c29-d4bd-2fa1-110e77de1c50.png)

That's me.

I'm sweet, I'm kind.

(Notice: That's a lie, right?)

---

これは私です

私は優しくて、親切です

（※訳者ツッコミ：ウソやろｗ）

# 気付かないでしょ！（You won't notice it!）

（6:10～6:24）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/4a511f1b-5c68-ce9c-d72a-d715ea5bf6f4.png)

And a little pussycat in the room.

So, this talk is not going to be, why you all suck.

Well Actually it is but it's indirect.

You won't notice it!

You won't notice it!

---

部屋に小さな猫ちゃんがいます

だから、この話はしません … なんで最悪だ

ま、これは遠回しな皮肉です

気付かないでしょ！

気付かないでしょ！

# プログラマになる方法（How I'm Becoming a Programmer）

（6:25～7:51）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/06682704-a5e2-b9d8-9057-a3c486624847.png)

This is me putting on a happy face and what I'm gonna talk about is "how I'm becoming a programmer".

Yes, it's all about me!

Me! Me! Me!

No it's not here's the reason I'm saying "How I'm becoming a programmer".

I am sick! Sick!

Sick of people telling other people how to do things.

No one can tell you how to be a programmer how to be a designer how to be a good father or mother.

It's none of their business and what's more it's beyond their understanding.

No two of us are the same person they're not in the same environment in the same situation doing the same work on the same code base using the same tool set particularly for a JavaScript programmer.

So given all of those things, it's impossible to tell anybody the best way of doing anything.

There are no best practices.

So, I am gonna tell you what I do and you are free to ignore it or say "I may be interesting or what a fool he is whatever".

---

これは私の幸せそうな顔で、私は「プログラマーになる方法」について話すつもりです

はい、すべて私について、です！

私！、私！、私！

いいえ、そこは私が「プログラマーになる方法」と言っている部分ではありません

私は病気です！ 病気！

物事のやり方を他人に伝えることに、もう、うんざり

どのようにしてプログラマーになり、どのようにしてデザイナーになり、どのようにして良い父親または母親になることができるのかは、誰にも教えられません

それは仕事にもならず、さらには彼らの理解を超えています

特に、JavaScriptプログラマーが2人いたら、「同じ人」では無いため、同じ環境／同じ状況／同じ作業／同じコードベース／同じツールセットになることはありません

これら全てを踏まえると、何かを行う最良の方法を誰かに教えることは不可能です

ベストプラクティスはありません

だから、私が何をするか教えてあげるし、あなたはそれを好きに無視できるし、または「私は面白いかもしれないし、彼はなんて馬鹿なんだ」とか言うかもしれません

# 私の3つの目標（My Three Goals）

（7:54～8:56）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/d7400e25-5896-8f99-19c1-4747ba853d37.png)

So I am gonna tell you.

How I'm trying to become a better programmer now?

I added it up and I have been programming for something like 48 years and I think I have probably coded.

I'm not gonna say every single day, I know that's not true.

But every single day within you know 0.05% or something right most days vast majority of days in that time.

And I used to joke that you know people say "what do you do?" (Translator's comment: What does this mean?)

I say you French, and I go no, and they'd say. (Translator's comment: What does this mean?)

Okay, "What do you do?"

And I'd say well.

"I'm a programmer and one day I'm hoping to get it right you know."

Haha, that was a little joke. (Translator's comment: I didn't understand this joke.)

And I've now realized that's stupid.

Because I'm never gonna get it right and that's okay.

---

だから、私はあなたに言うつもりです

どのように私は、今より良いプログラマーになろうとしていますか？

私はそれを実現し、48年くらい、何らかのプログラミングをしていて、コーディングしてきたであろうと思います

それが毎日と言うつもりは無いし、実際そうでも無いし

でも毎日のうち、0.05％くらいは正しくて、そういう時間の日が大多数です

そして、あなたは人々が「何の仕事をしていますか？」と言うのを知っている、というジョークを言います（訳者コメント：どういうこと？）

私はあなたにフランス語を言い、私は行きません、そして彼らは言うでしょう（訳者コメント：これは一体、何のネタ？）

OK、「何の仕事をしていますか？」

私はこう言います

「私はプログラマーであり、いつか、あなたが正しく理解することを望んでいます」

ハハ、ちょっと冗談です（訳者コメント：何がジョークが分かりません…）

私は今、それが愚かであることを理解しました

私は、それを正しくするつもりはないので大丈夫

## 1. 私のやっていることで幸せに（Happy doing what I'm doing）

（8:57～9:13）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/e90e602a-6970-5815-56db-7f958feafad3.png)

So my three goals.

I want to be happy doing what I'm doing.

And that's a two edged goal I want to do something that makes me happy.

And I want to be happy while I'm doing that thing.

---

私の3つの目標

（1つ目は）自分のやっていることで、自分を幸せにしたい

それは、私のやっている何かにより幸せになるという、両刃の目標です

そして、それをやっている間、私は幸せになりたいのです

## 2. 開発することと学ぶこと（Developing and learning）

（9:17～10:02）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/b16c1ddf-c211-69bf-20b5-d65fcf1e47c1.png)

I really want to keep developing not as encoding but as developing as a human being, and learning.

I think the word for a developer that's not developing is maintenance programmer.

Or actually no, unemployed.

Because we of all the industries on the planet I think put the strongest demands on our participants to learn.

I don't think any other industry has the kind of half-life of information that we have.

It's measured in a small number of years, not decades, not centuries, maybe 5 years, 10 years.

---

（2つ目は）私は本当に、エンコーディングでは無い、人間としての開発を続けていきたいと願っており、そして学びたいです

開発していない開発者の言葉はメンテナンスプログラマーの言葉だと思います

または失業者の言葉でしょう

私達は、地球上のすべての産業において、参加者が学ぶことを最も強制されていると思います

他の業界には、私達が持っているような情報の半減期があるとは思いません

それは、数十年ではなく、数世紀ではなく、恐らく、5年、10年で測定されます

## 3. 世界をより良く変える（Changing the world for the better）

（10:05～12:03）
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/a8e79bce-df40-044f-0833-15a680d66f44.png)

And last, and obviously more modestly.

I think it's really important that we change the world for the better.

And that doesn't necessarily mean that we get new treaty signed with different countries or that we you know cure some disease.

I think we all recognize when what we do.

Has an impact.

When, what we do has made things better than they were.

And it can be better in a really small way.

---

そして最後に、明らかに、控えめに

私達は、世界をより良く変えることが、本当に重要だと思います

そして、それは必ずしも私達が、様々な国と署名した新しい条約を取得することや、あなたが幾つかの病気を治すことを意味するわけではありません

私達は皆、いつ何をするかを認識していると思います

インパクトがあります

ときに、私達の行動は、物事を以前よりも良くしました

そして、それは本当に小さな方法で、より良くできます

---

I remember when I was working in England in the 80s we worked at one point British Telecom had these terminals called press-tell (Translator's comment: I don't know "press-tell") terminals and they were 20... no 40 columns wide 24 columns deep, 8 colors and they connected over a 300 baud modem.

Eventually upgraded to I think of 1200 baud modem.

And they basically all you could display you start at the top and you wrote whatever 24 times 40 was characters and that was the screen and then he sent it again and that was the next screen.

And these took off for some reason, I have know you one. (Translator's comment: I couldn't hear the last phrase...)

And we produced one of much things as my company produced was a system for travel agents.

---

80年代、私がイギリスで働いていた先の1つ、ブリティッシュテレコムには、プレステル（？）と呼ばれるターミナルがあり、幅は20列 … いや40列あり、奥行きは24列、8色で、300ボーのモデムで接続されています

最終的に、1200ボーのモデムにアップグレードしました

基本的に、あなたが表示できる全ては、トップからスタートし、24回の40文字を書き、それが画面で、それを再び送ったものが次の画面でした

それでこれらは、なんだか上手くいきました

そして、私の会社が生産した多くのうちの1つは、旅行代理店向けのシステムでした

---

They could are make simple flight reservations online using this press-tell (Translator's comment: I don't know "press-tell") terminals

Because the other alternative was to use the airlines terminals, and they were like you know 4 years worth of training before he could even log into them.

So we did that.

And I always remember the first time I walked down a high street in England and I looked through a window and I saw my code running on one of their terminals.

And the sheer, pleasure that gave me just to see something I done was being used.

And I think that motivates a lot of us, right?

So, changing the world for the better is important.

---

このプレステル（？）ターミナルを利用して、オンラインで簡単なフライト予約ができます

他の選択肢は、航空会社のターミナルを使用することですが、それにログインするために必要な4年分の訓練とこれは同等です

私達はそれを実現しました

そして、イギリスの大通りを初めて歩いたとき、私はいつも窓を覗き、自分のコードが端末の1つで実行されているのを見ました

そして、私がしたことを見る喜びを、私に与えてくれました

それが私達の多くを動機づけていると思います、どうです？

そう、世界をより良い方向に変えることが重要です

# 終わり

ここまでの内容は、そこまでテクニカルな内容も少なく、前置きが長かったので、なかなか本題まで入っていきませんでしたが、次回は、下記から始まる具体的な内容になっていきます
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/155423/12f7e97d-2e4b-28fe-a584-1f3e4c7c1ccf.png)

それにしても、Dave Thomas節がなかなか独特で、流れや前後の文脈を読むことや、ノリを理解することが難しかったなぁ
