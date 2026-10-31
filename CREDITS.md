# お墓の町（仮）素材のクレジット

SANZU CALL（D:\アプリ\スレスパ風）の素材から、使う物だけをコピーした（`tools/copy_assets.py`）。SANZU 側は変更していない。
出どころは SANZU の CREDITS.md / assets/audio/sfx/CREDITS.md / assets/audio/amb/CREDITS.md で確認した（2026-10-28）。

| このゲームのファイル | 出どころ | ライセンス |
|---|---|---|
| assets/enemy/slit_woman.glb（口裂け女 = SANZU の「マスクの女」・14,504 三角形） | SANZU 自作（tools/blender/make_slit_woman.py で Blender を使って作成） | オリジナル |
| assets/models/hosp*.glb（ストレッチャー・車椅子・点滴スタンド・書類・棚・ベッド・遺体の冷蔵庫・ナースデスク・割れたガラス 等）と付属の絵 | SANZU 自作（tools/blender/make_hospital_pack*.py ほか） | オリジナル |
| assets/player/Characters_Lis.gltf と絵 | Quaternius「Zombie Apocalypse Kit」 https://quaternius.com | CC0 |
| assets/textures/（dirty_tiles・plastered_wall_02・damaged_plaster・damaged_concrete_floor）512px に縮小 | Poly Haven https://polyhaven.com | CC0 |
| assets/audio/hospital.ogg（環境音） | SANZU 自作合成（tools/audio/make_ambient.py。録音を含まない種類） | オリジナル |
| assets/audio/vo_kuchisake_idle_*, vo_kuchisake_tell_*（息・ささやきを原形が分からないほど加工） | freesound.org CC0 録音の加工（Female Breathing Heavily (2) — OwlStorm / Frightened Breathing — nickrave / Ghost Whispers — Litruv。SANZU の vo_manifest.json で確認） | CC0 1.0 |
| assets/audio/step_concrete_*, step_heavy_*, pickup_*, door_* | Kenney（Impact Sounds / RPG Audio）の加工＋合成（SANZU assets/audio/sfx/CREDITS.md） | CC0 1.0 |
| assets/audio/heartbeat_* | SANZU 自作合成 | オリジナル |
| assets/audio/synth/*.wav（水滴・低い「ずん」・蛍光灯・うなり・つかまった音） | このゲームの自作合成（tools/make_sfx.py） | オリジナル |
| assets/fonts/BIZUDGothic-Bold-sub.ttf（使う字だけに小さくした物） | BIZ UDGothic — Copyright 2022 The BIZ UDGothic Project Authors | SIL Open Font License 1.1（assets/fonts/OFL_BIZUDGothic.txt） |
| assets/bake/bake.png（床の暗がりと光の溜まり） | このゲームで生成（tools/map_hospital.py） | オリジナル |

## 使わなかった物（記録）
- `hosp_blood_trail`（血の跡）: 血なしの決まりのため使わない。
- 「口裂け女の女王」（kuchisake_queen.glb・125,222 三角形）: 重すぎるので使わない（ふつうの敵の「マスクの女」で足りた）。
- VOICEVOX: 使わない。
- 道具: Godot Engine（MIT）。ゲーム画面に Godot の表記を出すかは発売前にまとめて決める（SANZU と同じ扱い）。

## 追記 2026-10-29（第2版 廃病院 v2）
- assets/models/ に SANZU 自作の病院の小物を 44 点足した（手術室・ICU・レントゲン・薬局・ナースステーション・霊安室・ボイラー室・院長室・リネン倉庫・非常階段など。出どころは上と同じ SANZU 自作・オリジナル）。
- 血なしの決まりのため、全部の小物（前からの 22 点も）の色見本の絵の暗い赤（血の色）を、くすんだ茶色にぬりかえてコピーした（tools/copy_assets.py）。
- 使わない小物（血の跡・遺体の袋・拘束ベッド・保護室の壁・拘束衣・電気治療器・赤ちゃんの物・解剖台・標本・感染性ごみ）は入れていない。
- 字体 BIZUDGothic-Bold-sub.ttf は tools/make_font_subset.py で作り直した（ライセンスは同じ SIL OFL 1.1）。

## 追記 2026-10-29（第2版 フェーズ2: 隠れる・道具・「きれい？」）
- assets/audio/synth/ に自作合成の音を足した（tools/make_sfx.py。録音なし）: glass_step（ガラスを踏む）・bottle_break（薬瓶が割れる）・throw（投げる）・scissors（つかまった時のはさみ・画面は暗転）・locker_open（ロッカー・引き出しを開ける）・hide（隠れる・出る）・ofuda（お札の青い火）・kirei_tone（「きれい？」の間の耳鳴り）。オリジナル。
- assets/audio/vo_kuchisake_intro_0.ogg（「きれい？」の時のささやき・言葉は聞き取れない）: SANZU の同名ファイルのコピー。出どころは上の vo_kuchisake_idle_* と同じ freesound.org CC0 録音（Female Breathing Heavily (2) — OwlStorm / Ghost Whispers — Litruv）の加工（SANZU の vo_manifest.json で確認）。CC0 1.0。
- 「わたし、きれい？」の声（せりふ）は無い（VOICEVOX は使わない決まり）。字で出している。
- 廊下に SANZU 自作の hosp3_wall_lockers を2つ足した（隠れ場所）。出どころは上と同じ。

## 追記 2026-10-29（第2版 フェーズ3: 部屋の怪異・エンドの絵・案内）
- assets/enemy/slit_woman.glb を直した（tools/fix_slit_woman.py・Blender 5.2 で元の glb を読んで書き出し直し。元は tools/_backup_20261029_phase3/enemy/）: 首の筒を立て襟で隠す・襟と肩の箱の角を丸める・血の色（刃・マスクのにじみ・裂け目の赤）をさび色と暗いしわの色にぬりかえ。三角形 14,504 → 14,612。出どころは同じ SANZU 自作・オリジナル。服の白とびは Godot 側の材質の直し（scripts/enemy.gd の fix_materials）。
- assets/audio/synth/ に自作合成の音を足した（tools/make_sfx.py。録音なし）: monitor_beep・light_snap・lamp_click・shutter_roll・shutter_drop・drawer_slide・boiler_roar・knock・breath_behind。オリジナル。
- assets/textures/anomaly/（face_window・xray_film・xray_shadow）: このゲームで作った（口裂け女のモデルを Godot で撮った写真を tools/make_anomaly_tex.py で加工・レントゲン写真は描いた物）。オリジナル。
- assets/endings/（front・back・roof のエンドの絵）: このゲームで描いた（tools/make_endings.py・Python の絵の道具で生成。写真・AI の画像・ほかの素材は使っていない）。オリジナル。墓石に名前・戒名・宗教の印は入れていない。
- （2026-10-29 director 指摘の直し）口裂け女のコートの色を白に近い明るい灰色に戻し（頂点の色）、胸の形とボタンの位置を直した（tools/fix_slit_woman.py）。出どころは同じ SANZU 自作・オリジナル。三角形 14,612。レントゲンの影の絵は描き直した（tools/make_anomaly_tex.py・オリジナル）。

## 追記 2026-10-29（音の担当: 追跡の音 v2・テケテケ・ネオン街）
- assets/audio/synth/chase_loop.wav・caught_hit.wav を作り直した（tools/make_sfx_chase.py v2。前の版は tools/_backup_20261029_sound/）。自作合成・オリジナル。
- assets/audio/neon/ の音は全部このゲームの自作合成（録音・外の素材・人の声・音楽なし）。オリジナル。
  - テケテケ: teke_hit_0〜5・teke_pair_0〜2・teke_rush・teke_chase_bed・teke_caught（tools/make_sfx_teke.py）
  - 街: amb_street・neon_hum・vending_hum・fan_loop・neon_spark・crossing_far（tools/make_sfx_neon.py）
- 2026-10-29 スマホ用の版（tools/make_sfx_phone.py）: heartbeat_0/1・step_heavy_0/1・synth/sting・caught・sheet_rise・drone に、元の音から作った倍音と短い「トッ」（合成のノイズ）を足した。出どころとライセンスは元のまま（heartbeat は SANZU 自作・step_heavy は Kenney CC0 の加工・synth は自作）。元は tools/_backup_20261029_sound/phone_src/。
- 2026-10-29 assets/audio/neon/anomaly/*.wav（ネオン街の怪異12の音・17ファイル）: このゲームの自作合成（tools/make_sfx_neon_anomaly.py。録音・外の素材・人の声なし）。オリジナル。

## 追記 2026-10-29（3D 担当: テケテケのモデル・ネオン街の外壁）
- assets/models/teketeke/teketeke.glb・teketeke_hand.glb: このゲームの自作（tools/teketeke/ の Python と Blender 5.2 で、形・髪・絵・骨・動きを手続きで作った。写真・外の素材・AI の画像は使っていない）。オリジナル。
- assets/textures/neon_facade/facade_atlas.png・facade_atlas_n.png（外壁と地面の絵: モザイクタイル・二丁掛けタイル・吹きつけ・打ち放し・ALC・波板・アスファルト・歩道の平板）: このゲームの自作（tools/make_facade_atlas.py で手続きで生成。写真・外の素材なし）。オリジナル。
- （同じ日・種類を増やした）facade_atlas を 4x4 の 16 種に（石張り・小口タイル・金属パネル・木の縦格子・波トタン・はがれたモルタル・貼り紙の壁〈字は無し〉・網代張りの歩道を追加）。色 2048x2048・法線 1024x1024。同じく tools/make_facade_atlas.py の自作・オリジナル。

## 追記 2026-10-29 夜（音の担当: ネオン街の音 その2）
- assets/audio/neon/ に足した音（18ファイル・tools/make_sfx_neon2.py）は全部このゲームの自作合成（録音・外の素材・人の声・言葉・音楽・実在の機械やブランドの音なし）。オリジナル。
  - step_wet_0〜3・step_in_0〜1（プレイヤーの足音）・climb・locked・breaker_on・power_down・autodoor（チャイムなし）・train_far・arcade_loop（旋律の無いでたらめな電子音）・medal_loop・pc_hum・teke_breath（息・言葉ではない）・ask_sting
  - vending_hum.wav は作り直し（前の版は tools/_backup_20261029_sound/night/）。
- ネオン街で使い回した第一怪の音（出どころは上の表のまま）: pickup_0/1・door_0（Kenney CC0 の加工）・heartbeat_0/1（SANZU 自作）・synth/hide・drip・buzz・shutter_roll・locker_open（自作合成）。

## 追記 2026-10-30（Web 公開・ホーム画面のアイコン）
- assets/ui/pwa/icon_*.png（ホーム画面のアイコン「百」と裂けた口の線。血なし）: このゲームで作った（tools/make_pwa_icons.py・字は BIZ UDGothic Bold／SIL OFL 1.1）。オリジナル。
- Web 公開（GitHub Pages）には、この CREDITS.md・字体のライセンス（OFL_BIZUDGothic.txt）・Godot Engine のライセンス（GODOT_LICENSE.txt）を一緒に置く（tools/make_pages.py）。
