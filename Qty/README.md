Before you add this module, you need to add the template
"vendor/magento/module-catalog/view/frontend/templates/product/view/addtocart.phtml" 
into your theme. ONce the theme's template is used, you may change the html
<input type="number" name="qty" id="qty" value="<?= / @escapeNotVerified / $block->getProductDefaultQty() * 1 ?>" title="<?= / @escapeNotVerified / __('Qty') ?>" class="input-text qty" data-validate="<?= $block->escapeHtml(json_encode($block->getQuantityValidators())) ?>" />
to
<button type="button" id="minusQty" value="1">-</button> <input type="number" name="qty" id="qty" value="<?= / @escapeNotVerified / $block->getProductDefaultQty() * 1 ?>" title="<?= / @escapeNotVerified / __('Qty') ?>" class="input-text qty" data-validate="<?= $block->escapeHtml(json_encode($block->getQuantityValidators())) ?>" /> <button type="button" id="addQty" value="1">+</button>
