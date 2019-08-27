# CTOS: Compiler Testing for Optimization Sequences

CTOS is a novel compiler testing method based on differential testing for detecting compiler bugs caused by optimization sequences. This repository contains the testing results of CTOS over seven months and the results of comparison experiments for our paper .

Currently, the most of work is conducted on LLVM, which is a mature and widely used compiler infrastructure. Hundreds of analysis and transformation optimizations have been implemented in LLVM. For more information about LLVM, please referring the website of LLVM, http://llvm.org/.

## Tested Optimization

| **OPTIMIZATION**                                                 | **OPTIMIZATION**                                                 |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| -adce<br/>-aggressive-instcombine<br/>-alignment-from-assumptions<br/>-always-inline<br/>-argpromotion<br/>-barrier<br/>-bdce<br/>-break-crit-edges<br/>-called-value-propagation<br/>-callsite-splitting<br/>-canonicalize-aliases<br/>-consthoist<br/>-constmerge<br/>-constprop<br/>-correlated-propagation<br/>-dce<br/>-deadargelim<br/>-demanded-bits<br/>-die<br/>-div-rem-pairs<br/>-dse<br/>-early-cse<br/>-early-cse-memssa<br/>-ee-instrument<br/>-elim-avail-extern<br/>-extract-blocks<br/>-flattencfg<br/>-float2int<br/>-forceattrs<br/>-functionattrs<br/>-globaldce<br/>-globalopt<br/>-globalsplit<br/>-gvn<br/>-gvn-hoist<br/>-gvn-sink<br/>-hotcoldsplit<br/>-indvars<br/>-inferattrs<br/>-inline<br/>-instcombine<br/>-instsimplify<br/>-ipconstprop<br/>-ipsccp<br/>-irce<br/>-jump-threading<br/>-lazy-value-info<br/>-lcssa<br/>-lcssa-verification<br/>-libcalls-shrinkwrap | -licm<br/>-load-store-vectorizer<br/>-loop-accesses<br/>-loop-data-prefetch<br/>-loop-deletion<br/>-loop-distribute<br/>-loop-extract<br/>-loop-extract-single<br/>-loop-idiom<br/>-loop-instsimplify<br/>-loop-interchange<br/>-loop-load-elim<br/>-loop-predication<br/>-loop-reduce<br/>-loop-reroll<br/>-loop-rotate<br/>-loop-simplify<br/>-loop-simplifycfg<br/>-loop-sink<br/>-loop-unroll<br/>-loop-unroll-and-jam<br/>-loop-unswitch<br/>-loop-vectorize<br/>-loop-versioning<br/>-loop-versioning-licm<br/>-lower-expect<br/>-lowerinvoke<br/>-lowerswitch<br/>-mem2reg<br/>-memcpyopt<br/>-memdep<br/>-memoryssa<br/>-mergefunc<br/>-mergeicmps<br/>-mergereturn<br/>-mldst-motion<br/>-nary-reassociate<br/>-newgvn<br/>-partial-inliner<br/>-partially-inline-libcalls<br/>-pgo-memop-opt<br/>-post-inline-ee-instrument<br/>-prune-eh<br/>-reassociate<br/>-reg2mem<br/>-rewrite-symbols<br/>-rpo-functionattrs<br/>-scalar-evolution<br/>-scalarizer<br/>-sccp |
| **OPTIMIZATION**                                             | **OPTIMIZATION**                                             |
| -separate-const-offset-from-gep<br/>-simple-loop-unswitch<br/>-simplifycfg<br/>-sink<br/>-slp-vectorizer<br/>-slsr<br/>-speculative-execution | -sroa<br/>-strip<br/>-strip-dead-prototypes<br/>-structurizecfg<br/>-tailcallelim<br/>-transform-warning<br/>-verify |



## Reported Bugs

**reported_bugs.xlsx** is the full list of the reported bugs, including bug ID, optimization sequences for each bug, bug type, bug status. In 7 months, we have reported 5 types and 104 valid bugs, of which 21 have been confirmed and fixed. 47 unique
optimization are identified to be faulty and 15 of them are loop related optimizations. The detail information of each bug can be found on the bug repository of LLVM using the following URLs.

### Crash: 57
- https://bugs.llvm.org/show_bug.cgi?id=40423      
- https://bugs.llvm.org/show_bug.cgi?id=40422      
- https://bugs.llvm.org/show_bug.cgi?id=40431      
- https://bugs.llvm.org/show_bug.cgi?id=40432      
- https://bugs.llvm.org/show_bug.cgi?id=39626      
- https://bugs.llvm.org/show_bug.cgi?id=40421      
- https://bugs.llvm.org/show_bug.cgi?id=40454      
- https://bugs.llvm.org/show_bug.cgi?id=40841      
- https://bugs.llvm.org/show_bug.cgi?id=39645      
- https://bugs.llvm.org/show_bug.cgi?id=40898      
- https://bugs.llvm.org/show_bug.cgi?id=40899      
- https://bugs.llvm.org/show_bug.cgi?id=40915      
- https://bugs.llvm.org/show_bug.cgi?id=40938      
- https://bugs.llvm.org/show_bug.cgi?id=40926      
- https://bugs.llvm.org/show_bug.cgi?id=40928      
- https://bugs.llvm.org/show_bug.cgi?id=40929      
- https://bugs.llvm.org/show_bug.cgi?id=40933      
- https://bugs.llvm.org/show_bug.cgi?id=40931      
- https://bugs.llvm.org/show_bug.cgi?id=40934      
- https://bugs.llvm.org/show_bug.cgi?id=40930      
- https://bugs.llvm.org/show_bug.cgi?id=40932      
- https://bugs.llvm.org/show_bug.cgi?id=40927      
- https://bugs.llvm.org/show_bug.cgi?id=40925      
- https://bugs.llvm.org/show_bug.cgi?id=41105      
- https://bugs.llvm.org/show_bug.cgi?id=40109      
- https://bugs.llvm.org/show_bug.cgi?id=41096      
- https://bugs.llvm.org/show_bug.cgi?id=41104      
- https://bugs.llvm.org/show_bug.cgi?id=41107      
- https://bugs.llvm.org/show_bug.cgi?id=41108      
- https://bugs.llvm.org/show_bug.cgi?id=41287      
- https://bugs.llvm.org/show_bug.cgi?id=41288      
- https://bugs.llvm.org/show_bug.cgi?id=41321      
- https://bugs.llvm.org/show_bug.cgi?id=41632      
- https://bugs.llvm.org/show_bug.cgi?id=41694      
- https://bugs.llvm.org/show_bug.cgi?id=41695      
- https://bugs.llvm.org/show_bug.cgi?id=41696      
- https://bugs.llvm.org/show_bug.cgi?id=42016      
- https://bugs.llvm.org/show_bug.cgi?id=42194      
- https://bugs.llvm.org/show_bug.cgi?id=42246      
- https://bugs.llvm.org/show_bug.cgi?id=42264      
- https://bugs.llvm.org/show_bug.cgi?id=42268      
- https://bugs.llvm.org/show_bug.cgi?id=42274      
- https://bugs.llvm.org/show_bug.cgi?id=42421      
- https://bugs.llvm.org/show_bug.cgi?id=42422      
- https://bugs.llvm.org/show_bug.cgi?id=42400      
- https://bugs.llvm.org/show_bug.cgi?id=42612      
- https://bugs.llvm.org/show_bug.cgi?id=42613      
- https://bugs.llvm.org/show_bug.cgi?id=42611      
- https://bugs.llvm.org/show_bug.cgi?id=41294      
- https://bugs.llvm.org/show_bug.cgi?id=42640      
- https://bugs.llvm.org/show_bug.cgi?id=42431      
- https://bugs.llvm.org/show_bug.cgi?id=41484      
- https://bugs.llvm.org/show_bug.cgi?id=42751      
- https://bugs.llvm.org/show_bug.cgi?id=42737      
- https://bugs.llvm.org/show_bug.cgi?id=42787      
- https://bugs.llvm.org/show_bug.cgi?id=42788      
- https://bugs.llvm.org/show_bug.cgi?id=42808      

### Invalid IR: 13
- https://bugs.llvm.org/show_bug.cgi?id=41723
- https://bugs.llvm.org/show_bug.cgi?id=41542
- https://bugs.llvm.org/show_bug.cgi?id=41697
- https://bugs.llvm.org/show_bug.cgi?id=42018
- https://bugs.llvm.org/show_bug.cgi?id=41725
- https://bugs.llvm.org/show_bug.cgi?id=42444
- https://bugs.llvm.org/show_bug.cgi?id=42448
- https://bugs.llvm.org/show_bug.cgi?id=42449
- https://bugs.llvm.org/show_bug.cgi?id=42450
- https://bugs.llvm.org/show_bug.cgi?id=42451
- https://bugs.llvm.org/show_bug.cgi?id=41285
- https://bugs.llvm.org/show_bug.cgi?id=42660
- https://bugs.llvm.org/show_bug.cgi?id=42860

### Wrong Code: 24
- https://bugs.llvm.org/show_bug.cgi?id=41509
- https://bugs.llvm.org/show_bug.cgi?id=41511
- https://bugs.llvm.org/show_bug.cgi?id=41557
- https://bugs.llvm.org/show_bug.cgi?id=41633
- https://bugs.llvm.org/show_bug.cgi?id=41637
- https://bugs.llvm.org/show_bug.cgi?id=41558
- https://bugs.llvm.org/show_bug.cgi?id=41698
- https://bugs.llvm.org/show_bug.cgi?id=41699
- https://bugs.llvm.org/show_bug.cgi?id=41702
- https://bugs.llvm.org/show_bug.cgi?id=41703
- https://bugs.llvm.org/show_bug.cgi?id=41708
- https://bugs.llvm.org/show_bug.cgi?id=41721
- https://bugs.llvm.org/show_bug.cgi?id=41700
- https://bugs.llvm.org/show_bug.cgi?id=42050
- https://bugs.llvm.org/show_bug.cgi?id=42051
- https://bugs.llvm.org/show_bug.cgi?id=42081
- https://bugs.llvm.org/show_bug.cgi?id=42043
- https://bugs.llvm.org/show_bug.cgi?id=42275
- https://bugs.llvm.org/show_bug.cgi?id=42283
- https://bugs.llvm.org/show_bug.cgi?id=41720
- https://bugs.llvm.org/show_bug.cgi?id=42267
- https://bugs.llvm.org/show_bug.cgi?id=42750
- https://bugs.llvm.org/show_bug.cgi?id=42800
- https://bugs.llvm.org/show_bug.cgi?id=42804

### Performance: 9
- https://bugs.llvm.org/show_bug.cgi?id=40895
- https://bugs.llvm.org/show_bug.cgi?id=40900
- https://bugs.llvm.org/show_bug.cgi?id=40937
- https://bugs.llvm.org/show_bug.cgi?id=40949
- https://bugs.llvm.org/show_bug.cgi?id=40950
- https://bugs.llvm.org/show_bug.cgi?id=41289
- https://bugs.llvm.org/show_bug.cgi?id=41291
- https://bugs.llvm.org/show_bug.cgi?id=41320
- https://bugs.llvm.org/show_bug.cgi?id=41290

### Bug of Code Gen.
- https://bugs.llvm.org/show_bug.cgi?id=42452

## Comparison experiments
**comparsion_results.xlsx** contains the results of comparison experiments in Section 4.4. The testing programs, optimization sequences, and the original testing results are contained in the '**comparison_experiments**' directory. **xx.tar.xz** includes the tested programs in the experiment. For each tested program, the bug information of compiler is attached to the end of the file.
