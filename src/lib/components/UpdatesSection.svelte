<section class="py-20 border-b border-border">
	<div class="container-custom">
		<div class="grid grid-cols-1 md:grid-cols-2 gap-16">
			
			<!-- Left Column: CTA & Visual -->
			<div class="flex flex-col h-full">
				<div class="mb-8">
					<p class="font-mono text-xs text-muted mb-4">Start building</p>
					<h2 class="text-2xl font-medium mb-4">Build the future of fintech</h2>
					<p class="text-muted font-light mb-8 text-sm leading-relaxed max-w-md">
						Join thousands of developers building innovative financial applications with Plaid's secure API infrastructure
					</p>
					<div class="flex gap-3 mb-12">
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors flex items-center gap-2">
							GET API KEYS
							<svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
								<path d="M1 11L11 1M11 1H3M11 1V9" stroke="currentColor" stroke-width="1.5"/>
							</svg>
						</button>
						<button class="border border-border px-3 py-1.5 text-xs font-mono uppercase hover:bg-primary-50 transition-colors">
							VIEW DOCS
						</button>
					</div>
				</div>
				
				<!-- API Code Visual -->
				<div class="mt-auto w-full bg-gray-950 rounded border border-border overflow-hidden">
					<div class="bg-gray-900 px-4 py-2 border-b border-gray-800 flex items-center gap-2">
						<div class="w-3 h-3 rounded-full bg-red-500"></div>
						<div class="w-3 h-3 rounded-full bg-yellow-500"></div>
						<div class="w-3 h-3 rounded-full bg-green-500"></div>
						<span class="ml-4 text-gray-400 text-[10px] font-mono">plaid_api.js</span>
					</div>
					<div class="p-4 font-mono text-[10px] text-green-400 leading-relaxed">
						<div class="text-gray-500">// Initialize Plaid client</div>
						<div><span class="text-purple-400">const</span> client = <span class="text-blue-400">new</span> PlaidClient();</div>
						<div class="mt-2 text-gray-500">// Get account balance</div>
						<div><span class="text-purple-400">const</span> balance = <span class="text-purple-400">await</span> client.getBalance();</div>
						<div class="mt-2"><span class="text-blue-400">console</span>.log(balance);</div>
					</div>
				</div>
			</div>

			<!-- Right Column: Updates -->
			<div>
				<p class="font-mono text-xs text-muted mb-8">Customer success stories</p>
				
				<div class="space-y-12">
					<!-- Update 1 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">Case Study</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Moneybox: High-speed, low-fee payments</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								Moneybox implemented Plaid's Payment Initiation API to enable instant, high-speed, low-fee payment solutions for their customers. The integration allowed them to reduce payment processing costs while improving the user experience with faster transaction times.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Payments</span>
						</div>
					</div>

					<!-- Update 2 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">Case Study</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Placid Express: 50% reduction in support queries</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								By implementing Plaid's Identity product, Placid Express achieved a 50% reduction in customer service queries. The automated identity verification streamlined their onboarding process and significantly reduced friction for new users.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Identity</span>
						</div>
					</div>

					<!-- Update 3 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">Testimonial</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">Drop: Years of development saved</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								"We could have spent years building a data solution that wouldn't have come close to what Plaid provides." - Daniel Whiffing, Technical Lead at Drop
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Transactions</span>
						</div>
					</div>

					<!-- Update 4 -->
					<div class="flex gap-8 group">
						<div class="font-mono text-xs text-muted w-24 shrink-0 pt-1">Case Study</div>
						<div>
							<h3 class="font-medium text-sm mb-2 group-hover:text-accent transition-colors cursor-pointer">YouLend: Boosting loan approval rates</h3>
							<p class="text-xs text-muted leading-relaxed mb-3">
								YouLend uses Plaid to boost loan approval rates through better data access. Real-time transaction data enables more accurate underwriting decisions and faster loan approvals for small businesses.
							</p>
							<span class="bg-gray-100 text-[10px] px-1.5 py-0.5 rounded text-muted">Lending</span>
						</div>
					</div>
				</div>
			</div>

		</div>
	</div>
</section>
