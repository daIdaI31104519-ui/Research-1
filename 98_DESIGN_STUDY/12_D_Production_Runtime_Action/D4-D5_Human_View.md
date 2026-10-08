# 12-D4〜D5 — Human View（非正式設計候補の人間向け投影）

**Document Role:** Human Projection / Working Study Checkpoint  
**Status:** HUMAN RE-CHECKED CANDIDATE / NOT CURRENT DESIGN / NOT INDEPENDENT CANONICAL  
**Derived From:** [D4 Precision](./D4_精密設計候補.md) / [D5 Precision](./D5_精密設計候補.md)  
**Provenance:** 会話上のHuman ViewおよびHuman Re-checkをもとに、保存用に整理・再構成した資料。逐語転記ではない。  
**Rule:** PrecisionとHuman Viewが衝突する場合は原会話・Precision候補へ戻って検査し、Human Viewだけで新しいAuthorityを生成しない。

---

# Part A — D4 Scope / Conditions / Current Validity

## A1. Purpose
BOTに正式Authorizationがある場合でも、対象Action、条件、時間的効力、制限によって現在の適用関係は異なる。過去の許可だけで今後のすべての注文を許可しない。

## A2. Authorization Scope
BTC Spot注文がカバーされていてもETH Perpetualや資金移動まで許可されたとは限らない。Market ScopeやRisk Scopeとも異なる。

## A3. Scope Coverage
対象ActionがScopeに含まれることと、正式条件・他Authority・最終Execution Permissionの成立は別。

## A4. Conditions
正式に定義されたConditionそのものと、現在の充足・確認結果を区別。注文開始時だけの条件と継続条件は一律に扱わない。

## A5. Unknown Conditions
未確認のConditionは「成立した」でも「未成立と証明された」でもない。確認可能性自体が正式条件ならその意味を尊重。Unknownから新しいUniversal Blockを作らない。

## A6. Verification Freshness
昔のVerificationがあることは現在の許可の証明にはならない。確認情報が古いことだけで正式Authorizationが取消されたと決めることもできない。

## A7. Temporal Validity
Formal Effective、Suspension、Revocation、Expirationなどを区別する。現在のRestrictionは過去の正式事実を無言で書き換えない。

## A8. Current Applicability
「今回のAction / Material Effect / Context / 時点に正式Authorizationがどう適用されるか」。すべてのExecution Permissionをまとめて発行する仕組みではない。

## A9. Effective / Recorded / Discovery Time
正式な発効時刻、記録時刻、BOTが知った時刻は異なる。記録Timestampだけで正式効力や責任を自動証明しない。

## A10. Standing Authorization
反復操作を正式範囲で認め得る。無制限な時間・数量・Aggregate Effectを意味せず、毎回のHuman Approvalも一律に要求しない。

## A11. Restrictions
Suspension / Revocation / Expiration / Condition unavailableは区別する。特定Actionの制限は別の正当なDefensive Actionの全域停止ではない。

## A12. In-Flight
注文送信→取引所受付→部分約定の間でAuthorizationが変わり得る。最初に許可されていたから全部許可とは限らず、後からの制限で過去の行為が必ず不正化するわけでもない。

## A13. Multiple Authorizations
複数許可の単純合成では対象外Permissionは生まれない。正式な共同適用は排除しない。

## A14. Aggregate / Concurrent
BOT AとBがそれぞれ条件を満たしても、共有Risk Capacityを両方で使用できるとは限らない。確認とReservationは別。

## A15. Retry
同じ注文目的の再送でも、新しいAttemptへのAuthorizationが自動継承されるとは限らない。新Attemptから必ず二重約定するとも限らない。

## A16. Recovery
通信復旧は正式Revocationの解除を意味しない。一方、許可が存続しており正式条件が回復したなら利用できる場合はある。

## A17. Unknown / Conflicting
Current Authorizationの不明をExecution Permissionへ変えない。Unknownだけで他市場全域の強制停止も作らない。

## A18. Fast Safety
正式に認可されたSafety / Defenseの可能性を残す。「Safetyだから何でも許可」という無制限Permissionも作らない。

## A19. Historical Integrity
当時の条件、正式効力、行使・結果、Actorの認識、事後評価を必要な範囲で区別する。後の利益は過去の正式許可を創作しない。

## A20. Non-Goals
D4は必須中央認証Service、毎回の人間承認、固定Refresh頻度、注文取消・再送・Forced Exit手順を決めない。

### D4時間例（説明用、判定はApplicable Governanceに従う）

```text
T0  BOTへBTC SpotのStanding Authorization
T1  BOTが条件を確認
T2  正式Restrictionが発効
T3  BOTが注文送信
T4  BOTがRestrictionを認識
T5  取引所が受付
T6  一部約定
```

**何が言えるか:** Formal Effective Time、Actor Discovery、Action Attempt、Exchange Acceptance、Partial Fillを区別する。**何が言えないか:** このTimeLineだけでT3の正式適法性、T5/T6への効力、停止・取消方針を一律確定すること。

---

# Part B — D5 Multi-Action / Automated Exercise

## B1. Purpose
個別Actionの許可・条件確認・成功が、複数Action全体の許可・安全・完了を保証しない。複数Actionがあることだけで新しい承認も作らない。

## B2. Individual vs Multi-Action
Batchにまとめても、個別ActionのIdentity・Authorization・Execution Factは消えない。

## B3. Material Relationship
同じStrategyでも無関係な場合があり、別Marketでも同じCommon-Cause Riskを受ける場合がある。ラベルで独立性を決めない。

## B4. Action Set / Batch / Sequence
Batchへ新しいActionを追加しただけでは元のAuthorizationのCoverageは拡大しない。正式に変更可能なBatchがカバーされている場合は尊重する。Batchは自動Atomicではない。

## B5. Automated Attempt / Proper Exercise
BOTが注文できたことと、正式Authorityに従った適切な行使は異なる。

## B6. Actor / Delegation
複数BOTがあることと独立Risk Budgetが複数あることは異なる。CallerのAuthorizationはCalleeへ自動Grantを発生させないが、正当なDelegationを阻害しない。

## B7. Individual / Aggregate Authorization
個別許可だけで集合全体が適切とは限らない。新しいAggregate Approvalを必ず要求するわけでもない。

## B8. Standing Authorization
正当に認可されたBOTの反復行使は可能。ただし無制限な回数・数量・時間・Riskではない。

## B9. Shared Constraint
Capacityを確認しただけで予約したとはいえず、予約しただけで消費したともいえない。個別Condition成立はAggregate Constraint成立を自動証明しない。

## B10. Intended vs Observed Aggregate Effect
二つの注文でHedgeを予定しても片方がRejectedなら予定した相殺は未成立の可能性がある。Riskは必ず単純加算とは限らない。

## B11. Concurrency / Temporal
BOT AとBが同じ利用可能Capacityを確認しても、後から同時に使えば集合制約を超え得る。具体的Lock / Reservation方式は後続で決める。

## B12. Dependency / Sequence
Action Aの後にBが起きてもAが原因とは限らない。同じSignalに由来する別Actionは同一Actionでも必ずDuplicateでもない。

## B13. Partial Completion
Batch内の一部がFILLED、一部REJECTED、一部UNKNOWNという状況を保持。Batch Success Criteriaは正式定義によるため、全件成功を必須と勝手に決めない。

## B14. Retry / Duplicate
一つのIntentから複数Attemptが生じ得る。Idempotencyと正式Authorizationを混同しない。複数AttemptでもExternal Effectの数は自動推定できない。

## B15. Authorization Change
Batchの途中でRestrictionが発効し得る。先行Actionへの許可が後続全Actionを必ずカバーするわけではない。

## B16. Interference
SafetyがExposureを減らす間、Trading BOTがExposureを増やすような関係を識別する。ただし識別だけでOverride・Cancel権限は生まれない。

## B17. Compensation / Recovery
Hedge失敗後の反対売買は別Actionになり得る。「Recovery目的だから許可」は不可。既存の正式Safety / Recovery権限の適用は尊重する。

## B18. Safety / Defensive
正当なFast Safetyを妨げず、Safety Labelから無制限なPermissionも作らない。具体的優先関係はSafety Governance。

## B19. Unknown / Conflicting
個別Orderの状態が一部KnownでもAggregate ExposureはUnknownになり得る。UnknownをSafeやSystem全域の一律Blockへ自動変換しない。

## B20. Historical Integrity
Batchの成功・利益は全Constituent Actionの正式Authorizationを事後的に証明しない。個別ActionのMaterialな事実を残す。

## B21. Non-Goals
Mandatory Controller、Global Queue、Lock、Atomic Transaction、Reservation、Retry Algorithm、Safety Override、Forced LiquidationをD5が独自に決定しない。

### D5並行実行例（仮定）

```text
Shared Risk Capacity = 100 units
BOT A Proposed Risk = 60
BOT B Proposed Risk = 60

T1  BOT Aは100利用可能と観測
T2  BOT Bは100利用可能と観測
T3  BOT AがAuthority Exerciseを試みる
T4  BOT BがAuthority Exerciseを試みる

仮に加算可能なRiskなら、双方の追加Risk合計は120。
Individual Evaluationの成立 ≠ Aggregate Constraintの成立。
```

この例はD5がRisk Budget=100を定義したわけではなく、Concurrencyの意味的な破綻経路を示す仮定である。

---

## Human Re-check主要注意点

- Batch Success != Every Action Completed / Properly Authorized
- Same Signal != Same Action / Proven Duplicate
- Caller Authorization != New Callee Grant
- Material Interference Identified != Runtime Override
- Standing Authorization != Unlimited Aggregate Exercise
- Aggregate State Unknown != Safe / Global Block
- Implementation Not Fixed != Formal Constraint Waived

**Non-Authority:** Human ViewはPrecision CandidateからのProjectionであり、独立した新しいAuthority Sourceではない。
