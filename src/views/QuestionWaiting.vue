<template>
	<div>
		<div class="container"> 
			<div class="Topstory">
				<div class="Topstory-container">
					<div class="mainColumn">
						<div class="NewYear2020Banner">
							<a class="NewYear2020Banner-link" href="https://www.zhihu.com/special/19554421" target="_blank" rel="noopener noreferrer">
								<img class="NewYear2020Banner-image" src="https://static.zhihu.com/heifetz/assets/NewYear2020Banner.e5ccc19d.png"></a></div>
						<div class="Card QuestionWaiting-mainColumn">
					
			<div class="townav">
							<div class="townav m-2" v-for="(single,index) in tab" @click="change(index)" :key="index">
							
						<v-btn class="toenavtype townav-type " 
						rounded depressed color="#f0f2f4" :class="{ active: count == index }">
							
					<span class="sp"  v-html="icons[index]"></span>
							{{single}}
						
							
							</v-btn>
							</div>
															</div>
							<div>
								
							<div class="Questiontextmain">
								<div class="ListQuestionItem QuestionWaiting-questionItem" v-for="(single,index) in message[count]" :key="index">
									<a class="ListQuestionItem-title QuestionWaiting-questionItemTitle ListQuestionItem-title--noDetail">{{single.question.title}}</a>
									<div v-if="single.question.excerpt">
										<span class="RichText ztext" itemprop="text"  >{{single.question.excerpt.substring(0,30)}}...<span class="read-more link" @click="change(index)">
								<span class="Button Followtext-more Button--plain" type="button" style="color: #8590a6;" >显示全部
								
								<span style="display: inline-flex; align-items: center;">
								 ​<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--ArrowDown Followtext-arrowIcon" fill="currentColor" viewBox="0 0 24 24" width="24" height="24">
								<path fill-rule="evenodd" d="M 12 13 L 8.285 9.218 a 0.758 
								0.758 0 0 0 -1.064 0 a 0.738 0.738 0 0 0 0 1.052 
								l 4.249 4.512 a 0.758 0.758 0 0 0 1.064 0 l 4.246 
								-4.512 a 0.738 0.738 0 0 0 0 -1.052 a 0.757 0.757 
								0 0 0 -1.063 0 L 12.002 13 Z" /></svg>
								</span>
								</span>
								     </span><title />
									</span>
									
									
									</div>
									<div class="ListQuestionItem-tool">
										<div class="ListQuestionItem-mainTool">
											<a class="Button ListQuestionItem-writeAnswerButton Button--blue Button--withIcon Button--withLabel">
												<span style="display: inline-flex; align-items: center;">​
												<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Edit Button-zi" fill="currentColor" viewBox="0 0 24 24" width="1.2em" height="1.2em">
													<path d="M 4.076 16.966 a 4.19 4.19 0 0 1 1.05 -1.76 l 8.568 
													-8.569 a 0.524 0.524 0 0 1 0.741 0 l 2.928 2.927 
													a 0.524 0.524 0 0 1 0 0.74 l -8.568 8.57 c -0.49 0.49 
													-1.096 0.852 -1.761 1.051 l -3.528 1.058 a 0.394 0.394 0 
													0 1 -0.49 -0.488 l 1.06 -3.53 Z M 20.558 4.83 c 0.59 0.59
													 0.59 1.546 0 2.136 l -1.693 1.692 a 0.503 0.503 0 0 1 -0.712
													  0 l -2.812 -2.812 a 0.504 0.504 0 0 1 0 -0.712 l 1.693 -1.693 a
													   1.51 1.51 0 0 1 2.135 0 l 1.389 1.389 Z" /></svg></span>写回答</a>
													   <button class="Button QuestionWaiting-followButton Button--plain Button--grey" type="button">
														   <svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Plus" fill="currentColor" viewBox="0 0 24 24" width="16" height="16">
															   <path fill-rule="evenodd" d="M 13.491 10.488 s -0.012 -5.387 0 -5.998
															   c -0.037 -1.987 -3.035 -1.987 -2.997 0 c -0.038 1.912 0 5.998 0 5.998 
															   H 4.499 c -1.999 0.01 -1.999 3.009 0 3.009 s 5.995 -0.01 5.995 -0.01 v 
															   5.999 c 0 2.019 3.006 2.019 2.997 0 c -0.01 -2.019 0 -5.998 0 -5.998 s 
															   3.996 0.009 6.004 0.009 c 2.008 0 2.008 -3 -0.01 -3.009 h -5.994 Z" /></svg>关注问题</button>
															   <button class="Button QuestionWaiting-laterButton Button--plain Button--grey" type="button">
																   <svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Later" fill="currentColor" viewBox="0 0 24 24" width="24" height="24">
																	   <path fill-rule="evenodd" d="M 12.004 4.15 a 7.85 7.85 0 1 1 -5.772
																		13.17 a 0.85 0.85 0 0 1 1.25 -1.153 a 6.15 6.15 0 1 0 -1.559 -5.087 
																		l 1.208 0.343 a 0.542 0.542 0 0 1 0.112 0.996 l -2.597 1.42 a 0.542 
																		0.542 0 0 1 -0.732 -0.21 l -1.44 -2.561 a 0.542 0.542 0 0 1 0.62 
																		-0.787 l 1.182 0.334 a 7.852 7.852 0 0 1 7.728 -6.465 Z m -0.178 3.792 c 
																		0.385 0 0.7 0.31 0.7 0.69 l -0.003 3.495 l 2.564 1.693 c 0.315 0.207 0.425 
																		0.671 0.185 0.977 c -0.24 0.305 -0.69 0.33 -0.99 0.126 c 0 0 -2.53 -1.663 -2.844 
															-1.9 c -0.315 -0.236 -0.315 -0.551 -0.315 -0.551 l 0.003 -3.84 c 0 -0.38 0.315 -0.69 0.7 -0.69 Z" /></svg>稍后答</button>
															</div><div class="ListQuestionItem-subTool"><div class="QuestionWaiting-info">{{single.question.answer_count}} 个回答 · {{single.question.visit_count}} 个浏览</div>
															</div>
															</div>
															</div>
														</div>	
								
	<router-view/>
							</div>
						</div>
					</div>
					<div class="homeyoubar">
						<div>
							<div class="homeyoubar-1" style="width: 100%;">
								<div class="Card homeyoutext01">
									<a title="回答" class="homeyoutext01-navItem" target="_blank" rel="noopener noreferrer">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Paper homeyoutext01-navIcon" fill="currentColor" viewBox="0 0 24 24"
										 width="24" height="24">
											<path d="M 9.273 6.13 c -1.103 0 -1.439 0.064 -1.782 0.243 a 1.348 1.348 0 
					0 0 -0.576 0.564 c -0.183 0.336 -0.248 0.664 -0.248 1.743 v 6.64 c 0 1.079 0.065 1.407
					 0.248 1.743 c 0.135 0.247 0.323 0.431 0.576 0.564 c 0.343 0.18 0.68 0.243 1.782 0.243 h 5.454 c 1.103 
					 0 1.439 -0.064 1.782 -0.243 c 0.253 -0.133 0.44 -0.317 0.576 -0.564 c 0.183 -0.336 0.248 -0.664 0.248 -1.743 V 
					 8.68 c 0 -1.079 -0.065 -1.407 -0.248 -1.743 a 1.348 1.348 0 0 0 -0.576 -0.564 c -0.343 -0.18 -0.68 -0.243 -1.782 -0.243 
					 H 9.273 Z m 0 -1.63 h 5.454 c 1.486 0 2.025 0.151 2.568 0.436 c 0.543 0.284 0.97 0.7 1.26 1.232 c 0.29 0.532 0.445 1.059 
					 0.445 2.512 v 6.64 c 0 1.453 -0.155 1.98 -0.445 2.512 c -0.29 0.531 -0.717 0.948 -1.26 1.232 c -0.543 0.285 -1.082 0.436 
					 -2.568 0.436 H 9.273 c -1.486 0 -2.025 -0.151 -2.568 -0.436 a 2.997 2.997 0 0 1 -1.26 -1.232 C 5.155 17.3 5 16.773 5 15.32 
					 V 8.68 c 0 -1.453 0.155 -1.98 0.445 -2.512 c 0.29 -0.531 0.717 -0.948 1.26 -1.232 c 0.543 -0.285 1.082 -0.436 2.568 -0.436 Z 
					 M 8.5 8.576 v 1.467 h 7 V 8.576 h -7 Z m 0 2.609 v 1.467 h 7 v -1.467 h -7 Z m 0 2.608 v 1.468 h 4.667 v -1.468 H 8.5 Z" /></svg>
										<div class="homeyoutext01-navTitle">写回答</div>
									</a>
									<a title="写文章" class="homeyoutext01-navItem" target="_blank" rel="noopener noreferrer">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--WriteArticle homeyoutext01-navIcon" fill="currentColor"
										 viewBox="0 0 24 24" width="24" height="24">
											<path d="M 15.764 6.779 l -3.76 3.765 c -0.428 0.43 -0.555 0.567 -0.667 0.713 a 1.666 1.666 
							 0 0 0 -0.208 0.348 c -0.076 0.167 -0.137 0.344 -0.314 0.926 l -0.073 0.243 l 0.242 -0.074 c 0.58 
							 -0.177 0.757 -0.238 0.925 -0.314 c 0.13 -0.06 0.232 -0.12 0.347 -0.209 c 0.146 -0.112 0.282 -0.239 
							 0.712 -0.668 l 3.759 -3.766 l -0.963 -0.964 Z m 0.963 -0.965 l 0.963 0.965 l 0.685 -0.686 c 0.167 
							 -0.168 0.227 -0.263 0.253 -0.349 a 0.187 0.187 0 0 0 0 -0.12 c -0.026 -0.086 -0.086 -0.18 -0.253 
							 -0.348 l -0.148 -0.148 c -0.167 -0.167 -0.262 -0.228 -0.348 -0.254 a 0.187 0.187 0 0 0 -0.12 0 c 
							 -0.085 0.026 -0.18 0.087 -0.347 0.254 l -0.685 0.686 Z m 0.87 5.471 l 1.702 -1.705 v 5.549 c 0 
							 1.52 -0.158 2.07 -0.455 2.626 a 3.096 3.096 0 0 1 -1.287 1.29 c -0.555 0.297 -1.105 0.455 -2.623 
							 0.455 h -5.57 c -1.517 0 -2.068 -0.158 -2.622 -0.455 a 3.096 3.096 0 0 1 -1.287 -1.29 C 5.158 
							 17.2 5 16.65 5 15.13 v -5.58 c 0 -1.52 0.158 -2.071 0.455 -2.627 a 3.096 3.096 0 0 1 1.287 
							 -1.289 c 0.554 -0.297 1.105 -0.455 2.622 -0.455 h 3.497 l -1.702 1.705 H 9.364 c -1.126 0 
							 -1.47 0.066 -1.82 0.254 c -0.258 0.138 -0.45 0.33 -0.588 0.59 c -0.188 0.35 -0.254 0.694 
							 -0.254 1.822 v 5.58 c 0 1.128 0.066 1.472 0.254 1.822 c 0.138 0.259 0.33 0.452 0.588 0.59
							  c 0.35 0.188 0.694 0.254 1.82 0.254 h 5.57 c 1.127 0 1.47 -0.066 1.82 -0.254 c 0.258 
							  -0.138 0.45 -0.331 0.589 -0.59 c 0.187 -0.35 0.253 -0.694 0.253 -1.822 v -3.844 Z 
							  m 1.593 -7.121 l 0.148 0.147 c 0.33 0.33 0.502 0.616 0.594 0.918 c 0.09 0.301 0.09 
							  0.61 0 0.911 c -0.092 0.302 -0.265 0.587 -0.594 0.917 l -5.408 5.416 c -0.486 0.487 
							  -0.648 0.635 -0.845 0.786 a 3.02 3.02 0 0 1 -0.614 0.37 c -0.226 0.102 -0.433 0.176 
							  -1.091 0.376 l -0.852 0.26 a 1.021 1.021 0 0 1 -1.275 -1.277 l 0.26 -0.854 c 0.2 -0.659 
							  0.273 -0.866 0.375 -1.092 c 0.103 -0.227 0.218 -0.418 0.369 -0.616 c 0.15 -0.197 0.299 
							  -0.36 0.785 -0.846 l 5.407 -5.416 c 0.33 -0.33 0.614 -0.504 0.915 -0.595 c 0.301 -0.092 
							  0.61 -0.092 0.91 0 c 0.301 0.09 0.586 0.264 0.916 0.595 Z" /></svg>
										<div class="homeyoutext01-navTitle">写文章</div>
									</a>
									<div class="homeyoutext01-navItem">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--WritePin homeyoutext01-navIcon" fill="currentColor"
										 viewBox="0 0 24 24" width="24" height="24">
											<path d="M 17.13 5.52 V 3.5 h 1.35 v 2.02 h 2.02 v 1.35 h -2.02 V 8.9 h -1.35 
								V 6.86 H 15.1 V 5.52 h 2.03 Z m -0.17 4.9 h 1.7 v 4.76 c 0 1.5 -0.17 2.05 -0.46 2.6 
								c -0.3 0.55 -0.73 0.98 -1.28 1.27 c -0.54 0.3 -1.1 0.45 -2.6 0.45 h -5.5 c -1.5 0 
								-2.05 -0.16 -2.6 -0.45 c -0.55 -0.3 -0.98 -0.72 -1.27 -1.27 c -0.3 -0.55 -0.45 -1.1
								 -0.45 -2.6 v -5.5 c 0 -1.5 0.16 -2.06 0.45 -2.6 c 0.3 -0.55 0.72 -0.98 1.27 -1.28 
								 c 0.55 -0.3 1.1 -0.45 2.6 -0.45 h 4.78 v 1.7 H 8.8 c -1.12 0 -1.46 0.05 -1.8 0.24 
								 c -0.26 0.1 -0.45 0.3 -0.58 0.55 c -0.2 0.35 -0.26 0.7 -0.26 1.8 v 5.5 c 0 1.13 0.07 
								 1.47 0.26 1.8 c 0.13 0.27 0.32 0.46 0.58 0.6 c 0.34 0.18 0.68 0.25 1.8 0.25 h 5.5 c 
								 1.12 0 1.46 -0.06 1.8 -0.25 c 0.27 -0.13 0.46 -0.32 0.6 -0.58 c 0.18 -0.34 0.24 -0.68 
								 0.24 -1.8 V 10.4 l 0.02 0.02 Z m -3.86 -0.22 c 0.7 -0.16 1.45 0.06 1.98 0.6 c 0.83 
								 0.83 0.83 2.2 0 3.04 l -0.03 0.03 c -0.84 0.85 -2.2 0.85 -3.04 0 l -1.92 -2 a 0.628 
								 0.628 0 0 0 -0.88 0 l -0.04 0.04 c -0.25 0.28 -0.25 0.7 0 0.95 c 0.15 0.16 0.37 
								 0.22 0.57 0.17 c 0.4 -0.1 0.82 0.18 0.9 0.58 c 0.1 0.4 -0.16 0.82 -0.57 0.9 c 
								 -0.7 0.17 -1.46 -0.04 -1.98 -0.58 c -0.83 -0.85 -0.83 -2.2 0 -3.06 l 0.03 -0.02 
								 c 0.86 -0.85 2.2 -0.85 3.05 0 l 1.93 1.95 c 0.24 0.25 0.63 0.25 0.87 0 l 0.03 
								 -0.02 a 0.67 0.67 0 0 0 0 -0.93 a 0.687 0.687 0 0 0 -0.58 -0.17 c -0.4 0.1 -0.8 
								 -0.16 -0.9 -0.57 c -0.1 -0.4 0.16 -0.8 0.57 -0.9 l 0.01 -0.01 Z" /></svg>
										<div class="homeyoutext01-navTitle">写想法</div>
									</div>
									<div class="homeyoutext01-navItem">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--VideoCamera homeyoutext01-navIcon homeyoutext01-navIcon--video"
										 fill="currentColor" viewBox="0 0 24 24" width="20" height="20">
											<path d="M 15.375 14.74 V 6.75 c 0 -1.036 -0.84 -1.875 -1.875 -1.875 h -9 c 
						-1.036 0 -1.875 0.84 -1.875 1.875 v 10.5 c 0 1.036 0.84 1.875 1.875 1.875 h 9 
						c 1.036 0 1.875 -0.84 1.875 -1.875 v -2.51 Z m 2.25 -7.428 l 1.657 -1.435 a 
						2.625 2.625 0 0 1 4.343 1.985 v 8.276 a 2.625 2.625 0 0 1 -4.343 1.985 l -1.657 
						-1.435 v 0.562 a 4.125 4.125 0 0 1 -4.125 4.125 h -9 A 4.125 4.125 0 0 1 0.375 17.25 V 
						6.75 A 4.125 4.125 0 0 1 4.5 2.625 h 9 a 4.125 4.125 0 0 1 4.125 4.125 v 0.562 Z m 0 
						2.976 v 3.424 l 3.13 2.71 a 0.375 0.375 0 0 0 0.62 -0.284 V 7.862 a 0.375 0.375 0 0 0 
						-0.62 -0.284 l -3.13 2.71 Z" /></svg>
										<div class="homeyoutext01-navTitle">发视频</div>
									</div>
									<a title="稍后答" class="homeyoutext01AnswerLater homeyoutext01-navItem homeyoutext01-answerLater" style="transform: scale(1);"
									 href="#" target="_blank" data-za-detail-view-id="5370">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Later homeyoutext01-navIcon" fill="currentColor" viewBox="0 0 24 24"
										 width="24" height="24">
											<path fill-rule="evenodd" d="M 12.004 4.15 a 7.85 7.85 0 1 1 -5.772 13.17 a 0.85 0.85 0 0 1 1.25 -1.153 a 6.15 6.15 0 1 0 -1.559 -5.087 
								l 1.208 0.343 a 0.542 0.542 0 0 1 0.112 0.996 l -2.597 1.42 a 0.542 0.542 0 0 1 -0.732 -0.21 l -1.44 -2.561 a 0.542 0.542 0 0 1 0.62 
								-0.787 l 1.182 0.334 a 7.852 7.852 0 0 1 7.728 -6.465 Z m -0.178 3.792 c 0.385 0 0.7 0.31 0.7 0.69 l -0.003 3.495 l 2.564 1.693 c 0.315
								 0.207 0.425 0.671 0.185 0.977 c -0.24 0.305 -0.69 0.33 -0.99 0.126 c 0 0 -2.53 -1.663 -2.844 -1.9 c -0.315 -0.236 -0.315 -0.551 -0.315 
								 -0.551 l 0.003 -3.84 c 0 -0.38 0.315 -0.69 0.7 -0.69 Z" /></svg>
										<div class="homeyoutext01-navTitle">稍后答</div>
									</a><a title="草稿" class="homeyoutext01-navItem" href="/draft" target="_blank" rel="noopener noreferrer"
									 data-za-not-track-link="true">
										<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--BlankPaper homeyoutext01-navIcon" fill="currentColor"
										 viewBox="0 0 24 24" width="24" height="24">
											<path d="M 12.917 4 a 2 2 0 0 1 1.478 0.652 l 4.083 4.475 A 2 2 0 0 1 19 10.475 v 5.345 c 0 1.453 -0.155 1.98 -0.445 2.512 c -0.29 0.531 -0.717 
									 0.948 -1.26 1.232 c -0.543 0.285 -1.082 0.436 -2.568 0.436 H 9.273 c -1.486 0 -2.025 -0.151 -2.568 -0.436 a 2.997 2.997 0 0 1 -1.26 -1.232 C 
									 5.155 17.8 5 17.273 5 15.82 V 8.18 c 0 -1.453 0.155 -1.98 0.445 -2.512 c 0.29 -0.531 0.717 -0.948 1.26 -1.232 C 7.248 4.15 7.787 4 9.273 4 h
									  3.644 Z M 12 5.63 H 9.273 c -1.103 0 -1.439 0.064 -1.782 0.243 a 1.348 1.348 0 0 0 -0.576 0.564 c -0.183 0.336 -0.248 0.664 -0.248 1.743 v 
									  7.64 c 0 1.079 0.065 1.407 0.248 1.743 c 0.135 0.247 0.323 0.431 0.576 0.564 c 0.343 0.18 0.68 0.243 1.782 0.243 h 5.454 c 1.103 0 1.439 
									  -0.064 1.782 -0.243 c 0.253 -0.133 0.44 -0.317 0.576 -0.564 c 0.183 -0.336 0.248 -0.664 0.248 -1.743 V 11.3 H 14 a 2 2 0 0 1 -2 -2 V 5.63 Z
									   m 1.5 0.37 v 2.9 a 0.9 0.9 0 0 0 0.9 0.9 H 17 L 13.5 6 Z" /></svg>
										<div class="homeyoutext01-navTitle">草稿箱</div>
									</a>
								</div>
								
								<div class="Card CreatorEntrance">
									<a class="CreatorEntrance-link CreatorEntrance-Link--smallIcon" href="/creator"
									 target="_blank" data-za-detail-view-id="6848">
										<div class="CreatorEntrance-hint ProfileSideCreator-creatorEntranceHint CreatorEntrancePage-hint--smallIcon">
											<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Creator CreatorEntrance-creator" fill="currentColor"
											 viewBox="0 0 24 24" width="24" height="24">
												<path fill-rule="evenodd" d="M 15.075 15.388 l -3.024 3.024 a 4.041 4.041 0 0 0 -1.014 1.697 l -0.26 0.868 C 7.844 20.986
											4.91 21 2 21 c 0.026 -3.325 0 -3.304 0.59 -3.956 c 1.237 -1.368 6.251 -0.68 6.44 -2.976 c 0.043 -0.518 -0.36 -1.06
										    -0.725 -1.69 C 6.285 8.87 5.512 2 11.5 2 c 5.988 0 5.15 7.072 3.246 10.378 c -0.357 0.62 -0.795 1.217 -0.724 1.77
											c 0.073 0.571 0.477 0.958 1.053 1.24 Z m 5.402 1.672 c 0.523 0.55 0.523 0.646 0.523 3.94 a 535.11 535.11 0 0 0 -4.434
											-0.028 l 3.911 -3.912 Z m -7.88 2.699 c 0.111 -0.37 0.312 -0.705 0.584 -0.978 l 4.76 -4.76 a 0.291 0.291 0 0 1 0.412 
											0 l 1.626 1.626 a 0.291 0.291 0 0 1 0 0.411 l -4.76 4.76 c -0.272 0.273 -0.608 0.474 -0.978 0.585 l -1.96 0.588 a
											0.219 0.219 0 0 1 -0.272 -0.272 l 0.589 -1.96 Z m 9.157 -6.742 a 0.839 0.839 0 0 1 0 1.187 l -0.94 0.94 a 0.28
											0.28 0 0 1 -0.395 0 l -1.563 -1.563 a 0.28 0.28 0 0 1 0 -0.395 l 0.94 -0.94 a 0.839 0.839 0 0 1 1.187 0 l 0.771 0.771 Z" /></svg>

											<div class="CreatorEntrance-text">
												<div class="CreatorEntrance-indexPageTitle">
													<div class="css-3j2kqe">创作者中心<span class="css-1ntg9ig">去开通</span></div>
												</div>
											</div>
											<svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--ArrowRight CreatorEntrance-arrow CreatorEntrance-arrow--smallIcon"
											 fill="currentColor" viewBox="0 0 24 24" width="24" height="24">
												<path fill-rule="evenodd" d="M 9.218 16.78 a 0.737 0.737 0 0 0 1.052 0 l 4.512 -4.249 a 0.758 0.758 0 0 0 0 -1.063 L 10.27 
						7.22 a 0.737 0.737 0 0 0 -1.052 0 a 0.759 0.759 0 0 0 -0.001 1.063 L 13 12 l -3.782 3.716 a 0.758 
						0.758 0 0 0 0 1.063 Z" /></svg>
										</div>
									</a></div>
								<div class="Card">
									<ul class="homeyoubar-categoryList">
										<li class="homeyoubar-categoryItem">
											<a title="Live" class="Button Button--plain" style="color: rgb(255, 207, 0);" href="/lives" target="_blank"
											 type="button" data-za-not-track-link="true">
												<span class="homeyoubar-categoryIcon"><svg xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Live" fill="currentColor"
													 viewBox="0 0 24 24" width="24" height="24">
														<path d="M 13.693 10.354 l 1.634 -7.542 c 0.195 -0.901 -0.16 -1.083 -0.798 -0.39 l -9.18 9.97 c -0.638 0.693 -0.377 1.254 0.582 1.254 h 5.376 l -1.634 7.542 c -0.195 0.901 0.16 1.083 0.798 0.39 l 9.18 -9.97 c 0.638 -0.693 0.377 -1.254 -0.582 -1.254 h -5.376 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">Live</span></a></li>
										<li class="homeyoubar-categoryItem"><a title="书店" class="Button Button--plain" style="color: rgb(67, 212, 128);"
											 href="/pub/" target="_blank" type="button" data-za-not-track-link="true"><span class="homeyoubar-categoryIcon"><svg
													 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Ebook" fill="currentColor" viewBox="0 0 24 24" width="24"
													 height="24">
														<path fill-rule="evenodd" d="M 16 17.649 V 2.931 a 0.921 0.921 0 0 0 -0.045 -0.283 a 0.943 0.943 0 0 0 -1.182 -0.604 L 4.655 5.235 A 0.932 0.932 0 0 0 4 6.122 v 14.947 c 0 0.514 0.421 0.931 0.941 0.931 H 19.06 c 0.52 0 0.941 -0.417 0.941 -0.93 V 7.292 a 0.936 0.936 0 0 0 -0.941 -0.931 h -0.773 v 12.834 a 0.934 0.934 0 0 1 -0.83 0.924 L 6.464 21.416 c -0.02 0.002 2.94 -0.958 8.883 -2.881 a 0.932 0.932 0 0 0 0.653 -0.886 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">书店</span></a></li>
										<li class="homeyoubar-categoryItem"><a title="圆桌" class="Button Button--plain" style="color: rgb(0, 132, 255);"
											 href="/roundtable" target="_blank" type="button" data-za-not-track-link="true"><span class="homeyoubar-categoryIcon"><svg
													 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Org" fill="currentColor" viewBox="0 0 24 24" width="24"
													 height="24">
														<path d="M 10.786 8.41 a 8.938 8.938 0 0 0 -3.968 -2.528 c -0.305 -1.719 0.814 -3.337 2.442 -3.741 c 1.221 -0.405 2.646 0.101 3.46 1.011 c 1.045 1.38 0.915 3.64 0.814 4.348 c -0.102 1.315 -1.221 3.034 -1.323 3.135 c -0.305 -0.809 -0.814 -1.517 -1.425 -2.225 Z m -2.442 2.832 c -1.526 0.202 -3.052 1.01 -4.171 2.123 c -1.12 -0.404 -1.934 -1.314 -2.137 -2.427 c -0.316 -2.427 1.526 -3.64 2.849 -3.842 c 1.628 -0.371 2.849 0.505 4.07 1.415 c 1.146 1.012 2.035 2.63 2.035 2.73 c -0.916 -0.202 -1.832 -0.1 -2.646 0 Z m 4.986 0.303 c 0.509 -0.607 0.931 -1.586 1.12 -2.225 c 0.318 -1.039 0.61 -3.134 0.203 -4.651 c 1.323 -1.011 3.154 -1.011 4.477 0.303 c 1.235 1.146 1.017 2.933 0.814 3.438 c -0.663 1.581 -1.933 2.326 -3.256 2.832 c -1.221 0.404 -3.256 0.303 -3.358 0.303 Z m -2.645 1.011 c -0.51 0.607 -0.916 1.416 -1.221 2.326 c -0.407 1.314 -0.643 3.06 -0.102 4.55 c -1.323 1.011 -3.256 1.011 -4.477 -0.202 c -1.198 -1.124 -1.018 -2.932 -0.814 -3.438 c 0.599 -1.605 1.933 -2.326 3.256 -2.831 c 0.916 -0.304 3.256 -0.405 3.358 -0.405 Z m 9.259 -1.82 c 1.017 0.404 1.933 1.315 2.035 2.427 c 0.233 2.57 -1.526 3.64 -2.849 3.842 c -1.526 0 -2.85 -0.505 -4.07 -1.415 c -1.018 -0.81 -2.035 -2.528 -2.035 -2.63 c 0.916 0.203 1.831 0.102 2.645 0 c 1.628 -0.404 3.053 -1.112 4.274 -2.224 Z m -6.716 4.854 c 1.065 1.08 2.442 2.022 4.07 2.528 c 0.306 1.719 -0.814 3.235 -2.442 3.741 c -1.22 0.405 -2.645 -0.101 -3.46 -1.011 c -1.1 -1.481 -1.017 -3.54 -0.915 -4.247 c 0.102 -1.315 1.221 -3.034 1.323 -3.135 c 0.305 0.708 0.721 1.44 1.424 2.124 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">圆桌</span></a></li>
										<li class="homeyoubar-categoryItem"><a title="专栏" class="Button Button--plain" style="color: rgb(15, 136, 235);"
											 href="//zhuanlan.zhihu.com" target="_blank" type="button" data-za-not-track-link="true"><span class="homeyoubar-categoryIcon"><svg
													 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Edit" fill="currentColor" viewBox="0 0 24 24" width="24"
													 height="24">
														<path d="M 4.076 16.966 a 4.19 4.19 0 0 1 1.05 -1.76 l 8.568 -8.569 a 0.524 0.524 0 0 1 0.741 0 l 2.928 2.927 a 0.524 0.524 0 0 1 0 0.74 l -8.568 8.57 c -0.49 0.49 -1.096 0.852 -1.761 1.051 l -3.528 1.058 a 0.394 0.394 0 0 1 -0.49 -0.488 l 1.06 -3.53 Z M 20.558 4.83 c 0.59 0.59 0.59 1.546 0 2.136 l -1.693 1.692 a 0.503 0.503 0 0 1 -0.712 0 l -2.812 -2.812 a 0.504 0.504 0 0 1 0 -0.712 l 1.693 -1.693 a 1.51 1.51 0 0 1 2.135 0 l 1.389 1.389 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">专栏</span></a></li>
										<li class="homeyoubar-categoryItem"><a title="付费咨询" class="Button Button--plain" style="color: rgb(84, 120, 240);"
											 href="/consult" target="_blank" type="button" data-za-not-track-link="true"><span class="homeyoubar-categoryIcon"><svg
													 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--Infinity" fill="currentColor" viewBox="0 0 24 24" width="24"
													 height="24">
														<path d="M 11.267 10.188 h -2.69 a 0.26 0.26 0 0 0 -0.261 0.26 v 0.508 c 0 0.149 0.117 0.26 0.262 0.26 h 2.896 v 1.54 H 8.578 a 0.26 0.26 0 0 0 -0.262 0.259 v 0.508 c 0 0.15 0.117 0.26 0.262 0.26 h 2.896 v 2.31 c 0 0.139 0.119 0.257 0.265 0.257 h 0.522 a 0.258 0.258 0 0 0 0.265 -0.257 v -2.31 h 2.896 a 0.26 0.26 0 0 0 0.262 -0.26 v -0.508 a 0.257 0.257 0 0 0 -0.262 -0.26 h -2.896 v -1.54 h 2.896 a 0.26 0.26 0 0 0 0.262 -0.26 v -0.507 a 0.257 0.257 0 0 0 -0.262 -0.26 h -2.69 l 2.51 -2.636 a 0.26 0.26 0 0 0 -0.004 -0.366 l -0.423 -0.413 a 0.253 0.253 0 0 0 -0.36 0.01 L 12 9.418 L 9.545 6.784 a 0.248 0.248 0 0 0 -0.36 -0.011 l -0.423 0.413 a 0.264 0.264 0 0 0 -0.004 0.366 l 2.509 2.636 Z M 12 19.973 c -1.101 0 -2.16 -0.15 -3.152 -0.43 c -0.532 0.18 -5.27 2.177 -4.743 1.179 c 0.527 -0.998 1.58 -2.746 0.806 -3.25 C 3.11 15.936 2 13.822 2 11.486 C 2 6.8 6.477 3 12 3 s 10 3.8 10 8.487 s -4.477 8.486 -10 8.486 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">付费咨询</span></a></li>
										<li class="homeyoubar-categoryItem"><a title="百科" class="Button Button--plain" style="color: rgb(88, 104, 209);"
											 href="/wiki" target="_blank" type="button" data-za-not-track-link="true"><span class="homeyoubar-categoryIcon"><svg
													 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--KnowledgeBase" fill="currentColor" viewBox="0 0 24 24"
													 width="24" height="24">
														<path d="M 21 9.749 v 9.91 c 0 0.74 -0.604 1.341 -1.35 1.341 H 4.35 C 3.604 21 3 20.4 3 19.659 V 9.319 c 0 -0.503 0.283 -0.963 0.733 -1.193 l 4.892 -2.5 V 3.341 c 0 -0.74 0.604 -1.341 1.35 -1.341 c 0.267 0 0.527 0.078 0.749 0.225 l 9.675 6.408 c 0.375 0.249 0.601 0.668 0.601 1.116 Z M 8.297 8.307 L 5.372 9.802 A 0.223 0.223 0 0 0 5.25 10 v 8.54 c 0 0.124 0.1 0.224 0.225 0.224 h 8.586 a 0.223 0.223 0 1 0 0.124 -0.41 l -4.959 -3.259 a 1.339 1.339 0 0 1 -0.601 -1.116 V 8.506 a 0.224 0.224 0 0 0 -0.328 -0.199 Z" /></svg></span><span
												 class="homeyoubar-categoryLabel">百科</span></a></li>
									</ul>
								</div>
								<div class="Pc-card Card"><a class="Banner-link" href="https://gitee.com/enterprises?utm_source=zhgg&amp;utm_medium=disp&amp;utm_campaign=enterprise&amp;utm_term=kfry8"
									 target="_blank">
										<div class="Banner-adTag">广告</div><img class="Banner-image" alt="广告" src="https://pic3.zhimg.com/v2-420a868112a60ceeed838ea3fbb3780e_540x450.png">
									</a>
									<div class="Pc-card-button-close " data-tooltip="不再显示" data-tooltip-position="bottom"><svg xmlns="http://www.w3.org/2000/svg"
										 class="Icon Icon--close Pc-card-button-close-svg " viewBox="0 0 12 12">
											<path fill-rule="evenodd" d="M 3 2 L 2 3 l 3 3 l -3 3 l 1 1 l 3 -3 l 3 3 l 1 -1 l -3 -3 l 3 -3 l -1 -1 l -3 3" /></svg></div>
								</div>
								<div class="Card">
									<ul class="homeyoubar-navList">
										<li class="homeyoubar-navItem homeyoubar-starItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/collections" target="_blank" type="button" data-za-not-track-link="true"><svg xmlns="http://www.w3.org/2000/svg"
												 class="Zi Zi--Star homeyoubar-navIcon" fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 5.515 19.64 l 0.918 -5.355 l -3.89 -3.792 c -0.926 -0.902 -0.639 -1.784 0.64 -1.97 L 8.56 7.74 l 2.404 -4.871 c 0.572 -1.16 1.5 -1.16 2.072 0 L 15.44 7.74 l 5.377 0.782 c 1.28 0.186 1.566 1.068 0.64 1.97 l -3.89 3.793 l 0.918 5.354 c 0.219 1.274 -0.532 1.82 -1.676 1.218 L 12 18.33 l -4.808 2.528 c -1.145 0.602 -1.896 0.056 -1.677 -1.218 Z" /></svg><span
												 class="homeyoubar-navText">我的收藏</span><span class="homeyoubar-navNumber">0</span></a></li>
										<li class="homeyoubar-navItem homeyoubar-questionListItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/people/xiao-ban-wen-30/following/questions" target="_blank" type="button" data-za-not-track-link="true"><svg
												 xmlns="http://www.w3.org/2000/svg" class="Zi Zi--HelpBubble homeyoubar-navIcon" fill="currentColor"
												 viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 5.74 4 h 12.52 c 0.961 0 1.74 0.775 1.74 1.73 V 16.27 c 0 0.955 -0.779 1.73 -1.74 1.73 h -3.825 l -1.658 2.044 a 1 1 0 0 1 -1.554 0 l -1.658 -2.044 H 5.74 C 4.78 18 4 17.224 4 16.27 V 5.73 C 4 4.775 4.778 4 5.74 4 Z M 12 16 a 0.976 0.976 0 0 0 0.705 -0.287 a 0.951 0.951 0 0 0 0.295 -0.712 a 0.954 0.954 0 0 0 -0.295 -0.714 A 0.976 0.976 0 0 0 12 14 a 0.962 0.962 0 0 0 -0.705 0.295 A 0.961 0.961 0 0 0 11 15 c 0 0.284 0.098 0.522 0.295 0.713 A 0.975 0.975 0 0 0 12 16 Z m 1.278 -4.924 a 36.81 36.81 0 0 0 1.023 -0.975 c 0.19 -0.193 0.354 -0.422 0.492 -0.688 c 0.138 -0.266 0.207 -0.575 0.207 -0.928 c 0 -0.448 -0.12 -0.864 -0.363 -1.246 a 2.517 2.517 0 0 0 -1.029 -0.906 C 13.164 6.111 12.652 6 12.072 6 c -0.624 0 -1.17 0.133 -1.638 0.399 c -0.468 0.265 -0.824 0.6 -1.068 1.005 c -0.244 0.405 -0.366 0.804 -0.366 1.2 c 0 0.19 0.077 0.368 0.231 0.531 a 0.747 0.747 0 0 0 0.567 0.246 c 0.38 0 0.638 -0.234 0.774 -0.703 c 0.144 -0.449 0.32 -0.788 0.528 -1.019 c 0.208 -0.23 0.532 -0.345 0.972 -0.345 c 0.376 0 0.683 0.114 0.921 0.342 c 0.238 0.229 0.357 0.51 0.357 0.841 c 0 0.17 -0.039 0.328 -0.117 0.473 a 1.782 1.782 0 0 1 -0.288 0.396 c -0.114 0.118 -0.3 0.294 -0.555 0.526 a 9.71 9.71 0 0 0 -0.696 0.688 c -0.172 0.194 -0.31 0.418 -0.414 0.673 a 2.391 2.391 0 0 0 -0.156 0.906 c 0 0.278 0.071 0.488 0.213 0.63 a 0.716 0.716 0 0 0 0.525 0.211 c 0.4 0 0.638 -0.216 0.714 -0.648 c 0.044 -0.203 0.077 -0.345 0.099 -0.426 c 0.022 -0.081 0.053 -0.162 0.093 -0.243 c 0.04 -0.081 0.101 -0.17 0.183 -0.268 c 0.082 -0.098 0.191 -0.21 0.327 -0.34 Z" /></svg><span
												 class="homeyoubar-navText">我关注的问题</span><span class="homeyoubar-navNumber">0</span></a></li>
										<li class="homeyoubar-navItem homeyoubar-inviteItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/question/invited" target="_blank" type="button" data-za-not-track-link="true"><svg xmlns="http://www.w3.org/2000/svg"
												 class="Zi Zi--Invite homeyoubar-navIcon" fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 4 10 V 8 a 1 1 0 1 1 2 0 v 2 h 2 a 1 1 0 0 1 0 2 H 6 v 2 a 1 1 0 0 1 -2 0 v -2 H 2 a 1 1 0 0 1 0 -2 h 2 Z m 10.455 2 c -2.21 0 -4 -1.79 -4 -4 s 1.79 -4 4 -4 s 4 1.79 4 4 s -1.79 4 -4 4 Z m -7 6 c 0 -2.66 4.845 -4 7.272 -4 C 17.155 14 22 15.34 22 18 v 1.375 c 0 0.345 -0.28 0.625 -0.625 0.625 H 8.08 a 0.625 0.625 0 0 1 -0.625 -0.625 V 18 Z" /></svg><span
												 class="homeyoubar-navText">我的邀请</span><span class="homeyoubar-navNumber">14</span></a></li>
										<li class="homeyoubar-navItem homeyoubar-balanceItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/balance" target="_blank" type="button" data-za-not-track-link="true"><svg xmlns="http://www.w3.org/2000/svg"
												 class="Zi Zi--Balance homeyoubar-navIcon" fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 19 19.5 H 5 a 2 2 0 0 1 -2 -2 V 7 a 2 2 0 0 1 2 -2 h 14 a 2 2 0 0 1 2 2 v 10.5 a 2 2 0 0 1 -2 2 Z m 0 -12 a 0.5 0.5 0 0 0 -0.5 -0.5 h -13 a 0.5 0.5 0 0 0 -0.5 0.5 v 2 a 0.5 0.5 0 0 0 0.5 0.5 h 3.75 c 1 0 1 2 2.75 2 s 1.75 -2 2.75 -2 h 3.75 a 0.5 0.5 0 0 0 0.5 -0.5 v -2 Z" /></svg><span
												 class="homeyoubar-navText">我的余额</span></a></li>
										<li class="homeyoubar-navItem homeyoubar-serviceItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/community" target="_blank" type="button" data-za-not-track-link="true"><svg xmlns="http://www.w3.org/2000/svg"
												 class="Zi Zi--Community homeyoubar-navIcon" fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 5.74 4 h 12.52 c 0.961 0 1.74 0.775 1.74 1.73 V 16.27 c 0 0.955 -0.779 1.73 -1.74 1.73 h -3.825 l -1.658 2.044 a 1 1 0 0 1 -1.554 0 l -1.658 -2.044 H 5.74 C 4.78 18 4 17.224 4 16.27 V 5.73 C 4 4.775 4.778 4 5.74 4 Z M 7 8.98 c 0 0.554 0.449 0.996 1.003 0.996 h 4.994 A 0.992 0.992 0 0 0 14 8.981 a 0.997 0.997 0 0 0 -1.003 -0.995 H 8.003 A 0.992 0.992 0 0 0 7 8.98 Z m 0 4 c 0 0.554 0.446 0.996 0.995 0.996 h 8.01 a 0.993 0.993 0 0 0 0.995 -0.995 a 0.993 0.993 0 0 0 -0.995 -0.995 h -8.01 A 0.993 0.993 0 0 0 7 12.98 Z" /></svg><span
												 class="homeyoubar-navText">站务中心</span></a></li>
										<li class="homeyoubar-navItem homeyoubar-copyrightItem"><a class="Button homeyoubar-navLink Button--plain"
											 href="/copyright" target="_blank" type="button" data-za-not-track-link="true"><svg xmlns="http://www.w3.org/2000/svg"
												 class="Zi Zi--Copyright homeyoubar-navIcon" fill="currentColor" viewBox="0 0 24 24" width="18" height="18">
													<path fill-rule="evenodd" d="M 16.517 15.815 a 5.871 5.871 0 0 1 -4.481 2.078 a 5.865 5.865 0 0 1 -5.859 -5.857 a 5.865 5.865 0 0 1 5.859 -5.859 c 1.63 0 3.204 0.7 4.319 1.919 c 0.085 0.093 0.24 0.432 0.209 0.797 a 1.086 1.086 0 0 1 -0.436 0.779 c -0.248 0.193 -0.516 0.29 -0.797 0.29 c -0.402 0 -0.7 -0.198 -0.814 -0.314 A 3.473 3.473 0 0 0 12 8.575 a 3.464 3.464 0 0 0 -3.46 3.461 a 3.464 3.464 0 0 0 3.46 3.46 a 3.63 3.63 0 0 0 2.654 -1.181 c 0.136 -0.152 0.458 -0.306 0.806 -0.306 c 0.274 0 0.542 0.095 0.773 0.274 c 0.35 0.269 0.45 0.588 0.473 0.809 c 0.032 0.308 -0.072 0.585 -0.188 0.723 m 4.686 -7.699 C 20.67 6.883 19.96 5.82 19.07 4.929 c -0.891 -0.89 -1.954 -1.601 -3.188 -2.133 A 9.728 9.728 0 0 0 12 2 a 9.733 9.733 0 0 0 -3.883 0.796 c -1.234 0.532 -2.297 1.243 -3.186 2.133 c -0.891 0.891 -1.602 1.954 -2.134 3.187 A 9.713 9.713 0 0 0 2 12 a 9.752 9.752 0 0 0 0.797 3.883 c 0.531 1.233 1.242 2.296 2.134 3.186 c 0.89 0.891 1.953 1.602 3.186 2.134 A 9.725 9.725 0 0 0 12 22 a 9.72 9.72 0 0 0 3.883 -0.797 c 1.233 -0.532 2.296 -1.243 3.188 -2.134 c 0.89 -0.89 1.601 -1.953 2.132 -3.186 A 9.73 9.73 0 0 0 22 12 a 9.69 9.69 0 0 0 -0.797 -3.884" /></svg><span
												 class="homeyoubar-navText">版权服务中心</span></a></li>
									</ul>
								</div>



								<footer class="Footer">
									<a class="Footer-item" href="//liukanshan.zhihu.com/" target="_blank" rel="noopener noreferrer">刘看山</a>
									<span class="Footer-dot"></span><a class="Footer-item" href="/question/19581624" target="_blank" rel="noopener noreferrer">知乎指南</a>
									<span class="Footer-dot"></span><a class="Footer-item" href="/terms" target="_blank" rel="noopener noreferrer">知乎协议</a><span
									 class="Footer-dot"></span>
									<a class="Footer-item" href="/term/privacy" target="_blank" rel="noopener noreferrer">知乎隐私保护指引</a><br>
									<a class="Footer-item" href="/app" target="_blank">应用</a>
									<span class="Footer-dot"></span><a class="Footer-item" href="https://app.mokahr.com/apply/zhihu" target="_blank"
									 rel="noopener noreferrer">工作</a>
									<span class="Footer-dot"></span>
									<button class="Button OrgCreateButton" type="button">申请开通知乎机构号</button><br>
									<a class="Footer-item" href="https://zhuanlan.zhihu.com/p/51068775" target="_blank" rel="noopener noreferrer">侵权举报</a>
									<span class="Footer-dot"></span><a class="Footer-item" href="http://www.12377.cn" target="_blank" rel="noopener noreferrer">网上有害信息举报专区</a><br>
									<a class="Footer-item" href="https://tsm.miit.gov.cn/dxxzsp/" target="_blank" rel="noopener noreferrer">京 ICP
										证 110745 号</a><br>
									<a class="Footer-item" href="http://www.beian.miit.gov.cn" target="_blank" rel="noopener noreferrer">京 ICP 备
										13052560 号 - 1</a><br>
									<a class="Footer-item" href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010802020088"
									 target="_blank" rel="noopener noreferrer">

										<img src="https://pic3.zhimg.com/80/v2-d0289dc0a46fc5b15b3363ffa78cf6c7.png">京公网安备 11010802010035 号</a><br>
									<span class="Footer-item">互联网药品信息服务资格证书<br>（京）- 非经营性 - 2017 - 0067</span><span class="Footer-item">违法和不良信息举报：010-82716601</span><br>
									<a class="Footer-item" href="/jubao" target="_blank">儿童色情信息举报专区</a><br><a class="Footer-item" href="/certificates"
									 target="_blank">证照中心</a><br>
									<a class="Footer-item" href="/contact" target="_blank">联系我们</a><span> © 2020 知乎</span></footer>

							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
	</div>
</template>

<script>

	export default{

		data(){

			return{

				icons:[

					'<svg class="Zi Zi--Fire toenavtype-icon" fill="#8590a6"  viewBox="0 0 24 16" width="18" height="18"><path d="M14.553 20.78c.862-.651 1.39-1.792 1.583-3.421.298-2.511-.656-4.904-2.863-7.179.209 2.291.209 3.73 0 4.314-.41 1.143-1.123 1.983-1.91 2.03-1.35.079-2.305-.512-2.863-1.774-.676 1.25-.782 2.556-.318 3.915.31.906.94 1.684 1.89 2.333C7.144 20.131 5 17.336 5 14.022c0-2.144.898-4.072 2.325-5.4.062 2.072.682 3.598 2.13 4.822-.67-1.112-.734-2.11-.734-3.517 0-3.253 2.067-6.007 4.913-6.927a7.35 7.35 0 0 0 2.157 4.918C17.722 9.214 19 11.463 19 14.022c0 3.073-1.844 5.7-4.447 6.758z" fill-rule="evenodd"></path></svg>',

					'<svg class="Zi Zi--Seed toenavtype-icon" fill="#8590a6" viewBox="0 0 24 16" width="18" height="18"><path d="M10.558 9.842c.745 1.423 1.148 2.996 1.283 4.574a14.663 14.663 0 0 1 .052 1.125 16.067 16.067 0 0 1-.491 4.078l-.028.104a.232.232 0 0 1-.295.155l-.94-.302a.221.221 0 0 1-.148-.277l.018-.055a13.683 13.683 0 0 0 .234-.852 14.827 14.827 0 0 0 .4-2.89.225.225 0 0 0-.176-.223 11.89 11.89 0 0 1-1.383-.42 11.508 11.508 0 0 1-1.806-.86 10.681 10.681 0 0 1-2.98-2.581A10.213 10.213 0 0 1 3.23 9.784 10.388 10.388 0 0 1 2.49 8a10.772 10.772 0 0 1-.406-1.87 9.95 9.95 0 0 1-.062-1.922.229.229 0 0 1 .29-.2c1.707.321 3.366.97 4.806 1.964a10.75 10.75 0 0 1 3.44 3.87zm12.04-2.252l.01.002c.117.03.19.147.165.266a8.966 8.966 0 0 1-1.274 3.592 8.552 8.552 0 0 1-1.204 1.521 8.724 8.724 0 0 1-1.53 1.212 8.872 8.872 0 0 1-3.674 1.233c-.235.027-.47.045-.705.056a.225.225 0 0 0-.207.256c.034.262.084.522.148.778a.223.223 0 0 1-.162.269l-.859.218a.223.223 0 0 1-.273-.177 8.418 8.418 0 0 1-.102-2.458c.05-.469.14-.932.27-1.384a7.868 7.868 0 0 1 2.234-3.63c.062-.057.123-.114.189-.167l.193-.161c.065-.053.133-.103.2-.153.13-.104.273-.194.41-.289.144-.086.284-.178.432-.255.144-.084.296-.155.445-.229.152-.067.303-.136.46-.194.309-.118.625-.22.946-.296a8.357 8.357 0 0 1 1.947-.23 8.143 8.143 0 0 1 1.941.22z"></path></svg>',

					'<svg class="Zi Zi--New toenavtype-icon" fill="#8590a6" viewBox="0 0 24 16" width="18" height="18"><path d="M3.111 2.667H20.89c.614 0 1.111.497 1.111 1.11v14.091c0 .45-.272.857-.689 1.028l-8.73 3.585c-.462.19-.98.187-1.441-.007L2.679 18.9A1.111 1.111 0 0 1 2 17.876V3.778c0-.614.497-1.111 1.111-1.111zm2.503 10.75v-2.753h.064l2.024 2.753h.977V8.573H7.51v2.725h-.064L5.429 8.573h-.983v4.844h1.168zm7.526-.99h-2.088v-.99h1.964v-.907h-1.964v-.967h2.088v-.99H9.82v4.844h3.32v-.99zm3.992-1.978h.06l.809 2.968h1.155l1.265-4.844h-1.269l-.634 3.212h-.06l-.803-3.212h-.987l-.775 3.212h-.06l-.645-3.212h-1.28l1.266 4.844h1.162l.796-2.968z" fill-rule="evenodd"></path></svg>',

					'<svg class="Zi Zi--Creator toenavtype-icon" fill="#8590a6" viewBox="0 0 24 16" width="18" height="18"><path d="M15.075 15.388l-3.024 3.024a4.041 4.041 0 0 0-1.014 1.697l-.26.868C7.844 20.986 4.91 21 2 21c.026-3.325 0-3.304.59-3.956 1.237-1.368 6.251-.68 6.44-2.976.043-.518-.36-1.06-.725-1.69C6.285 8.87 5.512 2 11.5 2c5.988 0 5.15 7.072 3.246 10.378-.357.62-.795 1.217-.724 1.77.073.571.477.958 1.053 1.24zm5.402 1.672c.523.55.523.646.523 3.94a535.11 535.11 0 0 0-4.434-.028l3.911-3.912zm-7.88 2.699c.111-.37.312-.705.584-.978l4.76-4.76a.291.291 0 0 1 .412 0l1.626 1.626a.291.291 0 0 1 0 .411l-4.76 4.76c-.272.273-.608.474-.978.585l-1.96.588a.219.219 0 0 1-.272-.272l.589-1.96zm9.157-6.742a.839.839 0 0 1 0 1.187l-.94.94a.28.28 0 0 1-.395 0l-1.563-1.563a.28.28 0 0 1 0-.395l.94-.94a.839.839 0 0 1 1.187 0l.771.771z" fill-rule="evenodd"></path></svg>'

				],

				tab:["人气问题","潜力好文","新问题","人人答"],

				category:['popularity','potential','newProblem','everyone'],

				message:[[],[],[],[]],

				count:0,

				flag:[[],[],[],[]]

			}

		},

		methods:{

			change(index){

				this.count = index;

				let param = this.category[index]

				this.axios.get('/api/question-wait/'+param).then(res=>{

					this.message.splice(index,1,res.data.data.data);



					this.flag[index] = new Array(res.data.data.data.length)

					this.flag[index].fill(false);

					console.log(this.flag)

				})

			},

			// 点击阅读全文触发函数

			showMore(index){

				alert("进入函数")

				var count = this.count;

				this.flag[count].splice(index,1,true)

				console.log(this.flag)

			}

		},

		created() {

			this.change(0)

		}

		

	}

</script>
<style lang="scss" scoped>
	.Topstory-container {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-align: start;
		-ms-flex-align: start;
		align-items: flex-start;
		width: 1000px;

		margin: 10px auto;
	}
.TopstoryTabs-link.is-active {
    color: #0084ff;
    font-weight: 500;
}

	.mainColumn {
		-ms-flex-negative: 0;
		flex-shrink: 0;
		margin-right: 10px;
		margin-bottom: 0px;
		width: 694px;
	}

	.NewYear2020Banner {
		overflow: hidden;
		margin-bottom: 10px;
		border-radius: 2px;
	}

	.NewYear2020Banner-link {
		display: block;
	}

	.NewYear2020Banner-image {
		display: block;
		width: 100%;
	}
.Card {
    margin-bottom: 10px;
    background: #fff;
    overflow: hidden;
    border-radius: 2px;
    -webkit-box-shadow: 0 1px 3px rgba(26,26,26,.1);
    box-shadow: 0px 1px 3px rgba(26,26,26,0.1);
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}


	/*右边1*/
	.homeyoubar {
		-webkit-box-flex: 1;
		-ms-flex: 1 1;
		flex: 1 1;
		font-size: 14px;
	}

	.homeyoutext01,
	.homeyoutext01-navItem {
		display: -ms-flexbox;
		display: flex;
	}

	.homeyoutext01 {
		-ms-flex-wrap: wrap;
		flex-wrap: wrap;
		overflow: visible;
	}

	.homeyoutext01-navItem {
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		cursor: pointer;
		-webkit-box-flex: 0;
		-ms-flex: 0 0 98px;
		flex: 0 0 98px;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-ms-flex-direction: column;
		flex-direction: column;
		height: 94px;
		-webkit-box-pack: center;
		-ms-flex-pack: center;
		justify-content: center;
		position: relative;
	}

	.homeyoutext01,
	.homeyoutext01-navItem {
		display: -ms-flexbox;
		display: flex;
	}

	.homeyoutext01-navIcon {
		color: #8590a6;
		margin-bottom: 6px;
	}

	.homeyoutext01-navTitle {
		color: #444;
		font-size: 16px;
	}

	/*右边2*/
	.CreatorEntrance-Link--smallIcon {
		padding: 0 17px;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
	}

	.CreatorEntrance-hint,
	.CreatorEntrance-link {
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
	}

	.CreatorEntrance-link {
		position: relative;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-pack: center;
		-ms-flex-pack: center;
		justify-content: center;
		height: 100%;
	}

	.CreatorEntrance-Link--smallIcon .CreatorEntrancePage-hint--smallIcon {
		height: 52px;
		width: 100%;
		padding: 0;
		margin: 0 16px;
	}

	.CreatorEntrance-creator {
		width: 18px;
		height: 18px;
		margin-left: 3px;
		color: #8590a6;
	}

	.CreatorEntrance-creator {
		width: 18px;
		height: 18px;
		margin-left: 3px;
		color: #8590a6;
	}

	.CreatorEntrance-text {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-flex: 1;
		-ms-flex-positive: 1;
		flex-grow: 1;
		margin-left: 6px;
		line-height: 16px;
	}

	.CreatorEntrance-indexPageTitle {
		font-size: 14px;
		line-height: 1.4;
		margin-left: 3px;
		color: #8590a6;
	}

	.css-3j2kqe {
		box-sizing: border-box;
		margin: 0;
		min-width: 0px;
		display: -webkit-box;
		display: -webkit-flex;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: justify;
		-webkit-justify-content: space-between;
		-ms-flex-pack: justify;
		justify-content: space-between;
	}

	.css-1ntg9ig {
		box-sizing: border-box;
		margin: 0;
		min-width: 0px;
		color: #0084ff;
	}

	.CreatorEntrance-arrow {
		color: #8590a6;
	}

	.CreatorEntrance-arrow--smallIcon {
		position: relative;
		left: 4px;
	}

	/*右3*/
	.homeyoubar-categoryList {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-ms-flex-wrap: wrap;
		flex-wrap: wrap;
		margin: 20px 0 -5px;
		padding: 0 10px;
	}

	.homeyoubar-categoryItem {
		width: 33%;
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		margin-bottom: 25px;
	}

	.homeyoubar-categoryItem .Button {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-flex: 1;
		-ms-flex: 1 1;
		flex: 1 1;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		-ms-flex-direction: column;
		flex-direction: column;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		position: relative;
		cursor: pointer;
		color: currentColor;
	}

	.homeyoubar-categoryIcon {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: end;
		-ms-flex-align: end;
		align-items: flex-end;
		width: 25px;
		height: 25px;
		margin-bottom: 10px;
	}

	.homeyoubar-categoryLabel {
		font-size: 15px;
		color: #8590a6;
	}

	/*右4*/
	.Pc-card {
		position: relative;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		width: 100%;
		border-radius: 2px;
		overflow: hidden;
		-webkit-transition: height .3s, margin .3s, opacity .3s;
		transition: height .3s, margin .3s, opacity .3s;
	}

	.Pc-card .Banner-adTag {
		position: absolute;
		right: 5px;
		bottom: 5px;
		width: 45px;
		border: 1px solid #ebebeb;
		border-radius: 5px;
		color: #ebebeb;
		background-color: #000;
		opacity: 0.5;
		font-size: 12px;
		line-height: 27px;
		text-align: center;
	}

	.Pc-card img {
		display: block;
		width: 100%;
		border-radius: 2px;
	}

	.Icon {
		vertical-align: text-bottom;
		fill: currentColor;
	}

	.Pc-card-button-close {
		position: absolute;
		top: 12px;
		right: 12px;
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-pack: center;
		-ms-flex-pack: center;
		justify-content: center;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		width: 18px;
		height: 18px;
		padding: 0;
		border-color: transparent;
		border-radius: 50%;
		background-color: #1a1a1a;
		opacity: 0;
		-webkit-transition: opacity .3s;
		transition: opacity .3s;
	}

	.Pc-card-button-close-svg {
		width: 14px;
		height: 16px;
		fill: #fff;
	}

	/*右5*/
	.homeyoubar-navList {
		width: 100%;
		padding: 8px 0;
	}

	ol,
	ul {
		padding: 0;
		margin: 0;
	}

	.homeyoubar-navLink {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
		padding: 0 20px;
		height: 40px;
		overflow: hidden;
	}

	.homeyoubar-navIcon {
		fill: #8590a6;
	}

	.homeyoubar-navText {
		-webkit-box-flex: 1;
		-ms-flex: 1 1;
		flex: 1 1;
		margin: 0 10px;
		text-align: left;
	}

	.homeyoubar-navNumber {
		padding: 6px 10px;
		border-radius: 2px;
		background: #f6f6f6;
		color: #8590a6;
		font-size: 12px;
	}

	/*右6*/
	.OrgCreateButton {

		color: #8590a6;
		border: none;
		padding: 0;
	}

	.homeyoubar .Footer {
		color: #8590a6;
		padding: 0 0 0 5px;
	}

	.Footer {
		color: #8590a6;
		padding: 10px 0 10px 5px;
		font-size: 13px;
		line-height: 2;

	}

	.Footer-item {
		color: #8590a6;
		display: -webkit-inline-box;
		display: -ms-inline-flexbox;
		display: inline-flex;
		-webkit-box-align: center;
		-ms-flex-align: center;
		align-items: center;
	}

	.Footer-dot::after {
		color: #8590a6;
		margin: 0 5px;
		content: "\B7";
	}
	.Snavcss{
	    color: #0084ff;
	}
	/*导航*/
	.townav {
	  display: flex;
	  align-items: center;
	  height: 63px;
	  padding: 5px;
	  background-color: #fff;
	 .active {
	 	background-color: #e6f3ff;
	 	color: #0c89ff;
		
	 }
	 
	}
.townav-type {
    margin: 0 10px;
	
}

.toenavtype {
   width:105px;
   height: 30px;
   line-height: 30px;
   text-align: center;
   border-radius: 16px;
   margin: 8px;
   background-color: #f6f6f6;
   color: #646464;
   cursor: pointer;
   
   
}

 /*内容*/

 .Questiontextmain {
     padding: 0 20px;
 }
.QuestionWaiting-questionItem {
    border-bottom: 1px solid #f6f6f6;
}
.ListQuestionItem {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    padding: 17px 0 22px;
    position: relative;
}
.QuestionWaiting-questionItemTitle {
    margin-right: 26px;
}
.ListQuestionItem-title--noDetail {
    margin-bottom: 0px;
}
.ListQuestionItem-title {
    color: #1a1a1a;
    font-size: 18px;
    line-height: 27px;
    margin-bottom: 8px;
    font-weight: 600;
    font-synthesis: style;
}
.ListQuestionItem-mainTool, .ListQuestionItem-subTool, .ListQuestionItem-tool {
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
}
.ListQuestionItem-tool {
    margin-top: 17px;
}
.ListQuestionItem-writeAnswerButton {
    line-height: 28px;
    padding: 0;
    width: 94px;
}
.Button--blue {
    color: #0084ff;
    border-color: #0084ff;
}

.Button--withIcon.Button--withLabel .Button-zi {
    margin-right: 4px;
}
.QuestionWaiting-followButton {
    margin-left: 20px;
}
.QuestionWaiting-followButton, .QuestionWaiting-laterButton {
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    line-height: 28px;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
    margin-left: 10px;
    width: 96px;
}
.Button--link, .Button--plain {
    height: auto;
    padding: 0;
    line-height: inherit;
    background-color: transparent;
    border: none;
    border-radius: 0;
}
.Button--grey {
    color: #8590a6;
    border-color: #8590a6;
}
.QuestionWaiting-laterButton .Zi {
    margin-right: 4px;
}
.ListQuestionItem-subTool {
    margin-left: auto;
}
.QuestionWaiting-info {
    color: #8590a6;
    font-size: 14px;
}

</style>
