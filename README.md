# CollectionFlowlayout 

    // MARK:- collection flowlyout 
    let sectionInsets = UIEdgeInsets(top: 0, left: 5, bottom: 0, right: 5)
    let itemsPerRow: CGFloat = 1
    var flowLayout: UICollectionViewFlowLayout {
        let _flowLayout = UICollectionViewFlowLayout()
        
        let paddingSpace = sectionInsets.left * (itemsPerRow + 1)
        let availableWidth = view.frame.width - paddingSpace
        let widthPerItem = availableWidth / productcollectionitemsPerRow
        
        _flowLayout.itemSize = CGSize(width: widthPerItem, height: widthPerItem)
        
        _flowLayout.sectionInset = UIEdgeInsets(top: 0, left: 5, bottom: 0, right: 5)
        _flowLayout.scrollDirection = UICollectionView.ScrollDirection.horizontal
        _flowLayout.minimumInteritemSpacing = 0
        _flowLayout.minimumLineSpacing = 0
        // edit properties here
        return _flowLayout
    }
