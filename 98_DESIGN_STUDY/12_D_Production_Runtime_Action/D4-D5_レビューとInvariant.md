# 12-D4〜D5 — Review・Invariant追跡台帳

**Document Role:** Working Study / Review Decision & Invariant Registry  
**Status:** CLOSED CANDIDATE SUPPORTING RECORD / NOT FORMALLY ADOPTED / NOT CURRENT DESIGN  
**Scope:** D4-01〜D4-38 / D5-01〜D5-50  
**Sources:** 会話に表示されたClosure Decision、Precision Review、Human Re-check、Destruction Reviewの要約およびInvariant列挙。完全な逐語Reviewログではない。  
**Primary Precision:** [D4](./D4_精密設計候補.md) / [D5](./D5_精密設計候補.md)  
**Human Projection:** [D4-D5 Human View](./D4-D5_Human_View.md)

---

## 1. Review履歴（事実と身分）

| 設計 | 会話でのReview状態 | Invariants | Closure |
|---|---|---|---|
| D4 | Initial Precision → Destruction → Precision → Human View → Human Re-check | D4-01〜D4-38 | CLOSED CANDIDATE |
| D5 | Initial Precision → Destruction Review 17論点 → Precision Review 15論点 → Human View → Human Re-check 16論点 | D5-01〜D5-50 | CLOSED CANDIDATE |

**注意:** CLOSED CANDIDATEはFormal Adoptionではない。D1〜D3原Closure・Invariantは本台帳では未復元。追加の原資料がない限り番号・文面を推測で作らない。

## 2. D4 Invariants（38件）

| ID | Semantic Invariant |
|---|---|
| D4-01 | Authorization Exists ≠ Universal Scope Coverage |
| D4-02 | Scope Coverage ≠ Condition Satisfaction |
| D4-03 | Scope Coverage ≠ Current Execution Permission |
| D4-04 | Market Scope ≠ Authorization Scope |
| D4-05 | Same Action Label ≠ Same Scope Coverage |
| D4-06 | Technical Access ≠ Authorization Coverage |
| D4-07 | Condition Defined ≠ Condition Satisfied |
| D4-08 | Previously Satisfied ≠ Currently Satisfied |
| D4-09 | Condition Unknown ≠ Condition Satisfied |
| D4-10 | Condition Unknown ≠ Universal Block |
| D4-11 | Historical Authorization ≠ Current Authorization |
| D4-12 | Historical Validity ≠ Current Validity |
| D4-13 | Authorization Expiration ≠ Historical Nonexistence |
| D4-14 | Recovery ≠ Automatic Permission Revival |
| D4-15 | Standing Authorization ≠ Unlimited Action Coverage |
| D4-16 | Individual Coverage ≠ Aggregate Coverage |
| D4-17 | Paper Authorization ≠ Real-Capital Authorization |
| D4-18 | Authorization Change ≠ Automatic Historical Rewrite |
| D4-19 | Prior Verification ≠ Unlimited Future Applicability |
| D4-20 | In-Flight Effect ≠ Automatically Authorized / Unauthorized |
| D4-21 | Authorization Evidence Missing ≠ Proven Historical Absence |
| D4-22 | Current Applicability Unknown ≠ Permission Granted |
| D4-23 | Restriction Applicability ≠ Universal Revocation |
| D4-24 | Scope / Conditions / Validity Governance ≠ Mandatory Runtime Approval Pipeline |
| D4-25 | Formal Validity ≠ Verification Freshness |
| D4-26 | Formal Effective Time ≠ Actor Discovery Time |
| D4-27 | Valid at Initiation ≠ All Later Effects Automatically Covered |
| D4-28 | Authorization Revocation ≠ External Order Automatically Canceled |
| D4-29 | Composite Authorization ≠ Automatically Expanded Permission |
| D4-30 | Individual Condition Satisfaction ≠ Concurrent Aggregate Satisfaction |
| D4-31 | Technical Recovery ≠ Formal Authorization Reinstatement |
| D4-32 | Prior Authorized Attempt ≠ New Attempt Automatically Authorized |
| D4-33 | Condition Evidence Unavailable ≠ Condition Proven False / True |
| D4-34 | Current Applicability Governance ≠ Mandatory Central Approval Pipeline |
| D4-35 | Current Applicability ≠ Universal Final Execution Permission |
| D4-36 | Condition Evaluation Unknown ≠ Formal Condition Not Satisfied |
| D4-37 | Condition Verification ≠ Risk Capacity Reserved |
| D4-38 | Recorded Timestamp ≠ Proof of Formal Effective Time |

## 3. D5 Invariants（50件）

| ID | Semantic Invariant |
|---|---|
| D5-01 | Individual Action Authorization ≠ Aggregate Authorization |
| D5-02 | Multiple Actions ≠ Mandatory New Aggregate Approval |
| D5-03 | Action Set Membership ≠ Shared Authority Scope |
| D5-04 | Batch Identity ≠ Individual Action Identity |
| D5-05 | Batch Submitted ≠ Batch Fully Executed |
| D5-06 | Sequence Started ≠ Sequence Completed |
| D5-07 | Standing Authorization ≠ Unlimited Automated Exercise |
| D5-08 | Automated Exercise ≠ Mandatory Per-Action Human Approval |
| D5-09 | Same Actor ≠ Universal Authority Coverage |
| D5-10 | Multiple Actors ≠ Independent Risk Capacity |
| D5-11 | Repeated Exercise ≠ Unconditional Future Authorization |
| D5-12 | Authority Exercise ≠ External Execution Success |
| D5-13 | Individual Condition Satisfaction ≠ Aggregate Constraint Satisfaction |
| D5-14 | Shared Constraint Verification ≠ Resource Reservation |
| D5-15 | Resource Availability Observed ≠ Resource Exclusively Allocated |
| D5-16 | Individual Risk Bounded ≠ Aggregate Risk Bounded |
| D5-17 | Different Action Targets ≠ Independent Material Effects |
| D5-18 | Aggregate Effect ≠ Necessarily Simple Sum of Individual Effects |
| D5-19 | Concurrent Individual Approval ≠ Concurrent Aggregate Safety |
| D5-20 | Prior Action Success ≠ Subsequent Action Authorization |
| D5-21 | Partial Completion ≠ Full Completion |
| D5-22 | Partial Failure ≠ Automatic Total Failure |
| D5-23 | Partial Completion ≠ Automatic Rollback |
| D5-24 | Action Dependency ≠ Mandatory Runtime Sequence for Every Action |
| D5-25 | Same Action Intention ≠ Same Execution Attempt |
| D5-26 | Additional Attempt ≠ Automatically Additional External Effect |
| D5-27 | Prior Authorized Attempt ≠ New Attempt Automatically Authorized |
| D5-28 | Aggregate State Unknown ≠ Aggregate State Safe |
| D5-29 | Aggregate State Unknown ≠ Universal System Block |
| D5-30 | Aggregate Outcome Success ≠ Proper Authorization of Every Constituent Action |
| D5-31 | Batch Authorization ≠ Universal Authorization of Every Constituent Action |
| D5-32 | Intended Aggregate Effect ≠ Actual Aggregate Effect |
| D5-33 | Intended Hedge ≠ Achieved Hedge |
| D5-34 | Cancel Acknowledgement ≠ All Related Exposure Removed |
| D5-35 | Same Signal ≠ Same Operational Action |
| D5-36 | Different Strategy ≠ Independent Material Risk |
| D5-37 | Valid Earlier Observation ≠ Later Aggregate Constraint Satisfaction |
| D5-38 | Shared Standing Authorization ≠ Independent Unlimited Coverage per Actor |
| D5-39 | Compensation Purpose ≠ Compensation Authority |
| D5-40 | Temporal Order ≠ Causal Dependency |
| D5-41 | Batch Status Label ≠ Complete Constituent Outcome |
| D5-42 | Repeated Local Success ≠ Global Process Correctness |
| D5-43 | Action Group Label ≠ Material Aggregate Boundary |
| D5-44 | Group Membership Change ≠ Automatic Extension of Group Authorization |
| D5-45 | Observed Automated Attempt ≠ Proper Authority Exercise |
| D5-46 | Caller Authorization ≠ Callee Authority Grant |
| D5-47 | Shared Constraint Observed ≠ Capacity Exclusively Committed |
| D5-48 | Idempotent Technical Handling ≠ Authorization for Additional Attempt |
| D5-49 | Interference Identified ≠ Authority to Preempt / Cancel |
| D5-50 | Material Relationship Unresolved ≠ Proven Independent Actions |

## 4. D4レビューで維持する重要Boundary

- Authorization Scope / Conditions / Current Validityは意味上別。Current ApplicabilityはUniversal Final Execution Permissionではない。
- Formal Validity、Verification Freshness、Evidence Sufficiencyを混同しない。
- UnknownをPermissionにせず、条件FalseやGlobal Blockとも同一視しない。
- Formal Effective TimeとRecord / Discovery Timeを区別する。
- In-Flightに対する事後Restrictionを全過去に遡及しない。先行許可から全後続EffectのCoverageを推定しない。
- Standing Authorizationを無制限にせず、普遍的Per-Action Human Approvalを要求しない。
- Recoveryによって失効したAuthorizationを無条件に復活させない。
- Condition VerificationはAggregate Risk Capacity Reservationではない。
- D4はClock、State Machine、Lock、Order Cancel、Safety Overrideなどの実装規則を作らない。

D4 Human Re-checkでは、会話上13件の説明明確化が採用候補。原詳細は会話履歴参照。追加InvariantのうちD4-35〜38は上記Invariant表に含む。

## 5. D5 Destruction Review（17論点と修正）

| ID | Failure / Attack | 必要なSemantic Repair |
|---|---|---|
| DR-D5-01 | 複数BOTが同じCapacityを利用 | Individual EvaluationとAggregate Constraintを分離 |
| DR-D5-02 | Verification後の状態変化 | Observation時点とExercise時点を区別 |
| DR-D5-03 | Batchに権限外Actionを混入 | Group MembershipとFormal Scopeを区別 |
| DR-D5-04 | Batchの一部しか執行されない | Intended / Actual、Constituent Outcomeを保持 |
| DR-D5-05 | Hedgeの片方だけ約定 | Intended Hedge != Achieved Hedge |
| DR-D5-06 | Cancel AcknowledgementでExposure消滅を推定 | Cancel Request / Effect / Exposureを区別 |
| DR-D5-07 | Retryで二重注文 | AttemptとExternal Effectの区別 |
| DR-D5-08 | 同じSignalから複数BOTが発注 | Shared Decision Originを保持 |
| DR-D5-09 | 別Strategy名でAggregate Riskを隠す | Material BoundaryはStrategy Labelではない |
| DR-D5-10 | Standing Authorizationの無制限複製 | Shared Authorization ≠ Independent Unlimited Coverage |
| DR-D5-11 | Batchの途中でRestriction | Constituent ActionのTemporal Applicabilityを保持 |
| DR-D5-12 | Compensationを無条件許可 | Purpose Label ≠ Authority |
| DR-D5-13 | Safetyと通常Actionが競合 | Interference != D5-Owned Priority |
| DR-D5-14 | Aggregate State Unknown | Unknown != Safe / Global Block |
| DR-D5-15 | 一部Failureを全体Failureと断定 | Status Labelと個別Outcomeを分離 |
| DR-D5-16 | Time Orderを因果と混同 | Temporal Order != Causal Dependency |
| DR-D5-17 | Action連鎖でRiskが累積 | Local Success != Global Process Correctness |

## 6. D5 Precision Review（15論点と対応）

| ID | Review Gate / Clarification | Revised Precision |
|---|---|---|
| PR-D5-01 | 新Aggregate Approvalの自動生成を排除 | §7 |
| PR-D5-02 | Batch Membership != Authorization Scope | §4 |
| PR-D5-03 | Automated Attempt != Proper Exercise | §5 |
| PR-D5-04 | Caller Authorization != Callee Authority Grant | §6 |
| PR-D5-05 | Standing Authorizationの共有 | §8 |
| PR-D5-06 | Observed / Reserved / Consumed Capacity | §9 |
| PR-D5-07 | 非単純加算のAggregate Effect | §10 |
| PR-D5-08 | Batch Labelと個別Outcome | §13 |
| PR-D5-09 | Idempotency != Authorization | §14 |
| PR-D5-10 | Time Order != Causal Dependency | §12 |
| PR-D5-11 | Batch途中のAuthorization変更 | §15 |
| PR-D5-12 | Compensation Purpose != Authority | §17 |
| PR-D5-13 | Safety Interference != Override | §16 / §18 |
| PR-D5-14 | Aggregate UnknownのMaterialなScope | §19 |
| PR-D5-15 | Mandatory Runtime Pipelineを作らない | §21 |

## 7. D5 Human Re-check（16誤読・説明修正）

| ID | 誤読防止の対象 | 説明のCorrection |
|---|---|---|
| HR-D5-01 | 複数ActionならAggregate Approval必須 | 新しいApprovalを自動要求しない |
| HR-D5-02 | 同じBatchなら全Actionをカバー | Batch Membership != Scope |
| HR-D5-03 | 技術的注文成功ならProper Exercise | Attempt / Proper / Outcomeを区別 |
| HR-D5-04 | Callerの権限がCalleeへ自動移る | Delegationは正式Governanceに従う |
| HR-D5-05 | BOT数だけCapacityが増える | Capacityは共有の可能性 |
| HR-D5-06 | Capacity確認なら確保済み | Observation != Reservation |
| HR-D5-07 | 別MarketならRisk独立 | Common-Cause Riskの可能性 |
| HR-D5-08 | Batchで一部失敗なら全体失敗 | Success Criteriaと個別Outcomeを区別 |
| HR-D5-09 | IdempotencyならRetryが認可済み | Technical Handling != Authorization |
| HR-D5-10 | 時系列なら因果関係 | Temporal != Causal |
| HR-D5-11 | Batch開始の許可は全後続に有効 | Current Applicabilityを尊重 |
| HR-D5-12 | Recoveryなら追加許可不要 | 正式Coverageを確認 |
| HR-D5-13 | Safetyという名称だけでAlways Override | Authorityを作らない |
| HR-D5-14 | Aggregate Unknownなら全域Block | Material Scopeを保持 |
| HR-D5-15 | 50 Invariantなら50新機能 | Semantic Invariantsであり新機能数ではない |
| HR-D5-16 | 必須Lockなし＝競合対策不要 | 実装未固定 != 正式制約の免除 |

## 8. Closure Review判定

D4 / D5の会話上のClosure Decisionはいずれも**CLOSED CANDIDATE**。D5 Closure Gate CG-D5-01〜08はSemantic BoundaryについてPASS候補。

**Formal Adoption NOT CONFIRMED.** Invariantが50件あることは50個の新規Governance Authorityや実装Classを意味しない。

## 9. 後続へ引き渡す未設計事項

Risk Formula、Aggregate Capacity、Reservation / Lock / Transaction、Batch Success Criteria、Partial Fill、Retry / Idempotency、Formal Delegation、Safety Priority、Compensation / Recovery、Event Log、Clock、Conflict Precedenceなどの**具体的方式**はそれぞれのApplicable Governanceへ委ねる。

これらの実装方法を未固定にすることは、Formal AuthorityやApplicable Constraintの迂回を許可することではない。

## 10. Reopen / Integrity

後続設計でD4またはD5の中心責任、Formal Authority、Current Applicability、Aggregate Effect、Historyの意味が変わる場合は元のSectionへ戻って再検査する。単に実装方式が決まっただけなら自動的に再設計する必要はない。

**D1〜D3のレビュー原文とInvariantの欠落は、回復待ちの既知事項であり、推測で捏造しない。**
